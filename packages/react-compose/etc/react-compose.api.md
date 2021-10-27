## API Report File for "@fluentui/react-compose"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import * as React_2 from 'react';

// @public (undocumented)
export interface BaseSlots {
    // (undocumented)
    root: React_2.ElementType;
}

// @public
export type ClassDictionary = Record<string, string>;

// @public
export type ClassFunction = (state: GenericDictionary, slots: GenericDictionary) => ClassDictionary;

// @public (undocumented)
export interface ComponentProps {
    // (undocumented)
    as?: React_2.ElementType;
    // (undocumented)
    className?: string;
}

// @public (undocumented)
export type ComponentWithAs<TElementType extends keyof JSX.IntrinsicElements = 'div', TProps = {}> = (<TExtendedElementType extends React_2.ElementType = TElementType>(props: Omit<PropsOfElement<TExtendedElementType>, 'as' | keyof TProps> & {
    as?: TExtendedElementType;
} & TProps) => JSX.Element) & {
    propTypes?: React_2.WeakValidationMap<TProps> & {
        as: React_2.Requireable<string | ((props: any, context?: any) => any) | (new (props: any, context?: any) => any)>;
    };
    contextTypes?: React_2.ValidationMap<any>;
    defaultProps?: Partial<TProps & {
        as: TElementType;
    }>;
    displayName?: string;
    readonly __PRIVATE_PROPS?: Omit<PropsOfElement<TElementType>, 'as' | keyof TProps> & {
        as?: TElementType;
    } & TProps;
};

// @public (undocumented)
export function compose<TElementType extends keyof JSX.IntrinsicElements, TInputProps, TInputStylesProps, TParentProps, TParentStylesProps>(input: Input<TElementType, TInputProps>, inputOptions?: ComposeOptions<TInputProps, TInputStylesProps, TParentProps, TParentStylesProps>): ComponentWithAs<TElementType, TInputProps & TParentProps>;

// @public (undocumented)
export type ComposedComponent<TProps = {}> = React_2.FunctionComponent<TProps> & {
    fluentComposeConfig: Required<ComposePreparedOptions>;
};

// @public (undocumented)
export type ComposeOptions<TInputProps = {}, TInputStylesProps = {}, TParentProps = {}, TParentStylesProps = {}, TState = TParentProps & TInputProps> = {
    className?: string;
    classes?: ClassDictionary | ClassFunction | (ClassDictionary | ClassFunction)[];
    displayName?: string;
    mapPropsToStylesProps?: (props: TParentStylesProps & TInputProps) => TInputStylesProps;
    handledProps?: (keyof TInputProps | 'as')[];
    overrideStyles?: boolean;
    slots?: Record<string, React_2.ElementType>;
    slotProps?: (props: TParentProps & TInputProps) => Record<string, object>;
    shorthandConfig?: ShorthandConfig<TParentProps & TInputProps>;
    state?: (props: TState, ref: React_2.Ref<HTMLElement>, options: ComposePreparedOptions) => any;
};

// @public
export type ComposePreparedOptions<TProps = {}, TInputState = any, TParentState = TProps> = {
    className: string;
    classes: (undefined | ClassDictionary | ClassFunction)[];
    displayName: string;
    displayNames: string[];
    mapPropsToStylesPropsChain: ((props: object) => object)[];
    render: ComposeRenderFunction;
    handledProps: (keyof TProps | 'as')[];
    overrideStyles: boolean;
    slots: Record<string, React_2.ElementType> & {
        __self: React_2.ElementType;
    };
    slotProps: ((props: TProps) => Record<string, object>)[];
    state: (props: TParentState, ref: React_2.Ref<HTMLElement>, options: ComposePreparedOptions) => TInputState;
    resolveSlotProps: <TResolvedProps>(props: TResolvedProps) => Record<string, object>;
    shorthandConfig: ShorthandConfig<TProps>;
};

// @public (undocumented)
export type ComposeRenderFunction<TElementType extends React_2.ElementType = 'div', TProps = {}, TState = TProps> = (props: TProps, ref: React_2.Ref<TElementType extends keyof HTMLElementTagNameMap ? HTMLElementTagNameMap[TElementType] : TElementType>, options: ComposePreparedOptions & {
    state: any;
}) => React_2.ReactElement | null;

// @public
export const createClassResolver: (classes: ClassDictionary) => (state: GenericDictionary) => ClassDictionary;

// @public
export type GenericDictionary = Record<string, any>;

// @public (undocumented)
export type Input<TElementType extends React_2.ElementType = 'div', TProps = {}> = InputComposeComponent<TProps> | ComposeRenderFunction<TElementType, TProps & {
    as?: React_2.ElementType;
}>;

// @public (undocumented)
export type InputComposeComponent<TProps = {}> = React_2.FunctionComponent<TProps> & {
    fluentComposeConfig?: Required<ComposePreparedOptions>;
};

// @public
export function mergeProps<TProps, TState = TProps, TSlots = GenericDictionary, TSlotProps = {
    [key in keyof TSlots]: any;
}>(state: TState, options: ComposePreparedOptions<TProps, TState>): MergePropsResult<TState, TSlots, TSlotProps>;

// @public (undocumented)
export type MergePropsResult<TState extends GenericDictionary, TSlots = GenericDictionary, TSlotProps = {
    [key in keyof TSlots]: any;
}> = {
    state: TState;
    slots: TSlots;
    slotProps: TSlotProps;
};

// @public
export function mergeSlotProp<TProps>(slotProp: SlotProp<TProps>, slotProps: TProps, mappedProp?: string): SlotProp<TProps>;

// @public (undocumented)
export type ObjectSlotProp<TProps extends GenericDictionary> = TProps & {
    children?: TProps['children'] | SlotPropRenderFunction<TProps>;
};

// @public (undocumented)
export type PropsOfElement<E extends keyof JSX.IntrinsicElements | React_2.JSXElementConstructor<any> | ComponentWithAs> = E extends {
    __PRIVATE_PROPS: any;
} ? E['__PRIVATE_PROPS'] : JSX.LibraryManagedAttributes<E, React_2.ComponentPropsWithRef<E>>;

// @public (undocumented)
export interface ShorthandConfig<TProps> {
    // (undocumented)
    allowsJSX?: boolean;
    // (undocumented)
    mappedArrayProp?: keyof TProps;
    // (undocumented)
    mappedProp?: keyof TProps;
}

// @public (undocumented)
export type SlotProp<TProps> = React_2.ReactChild | React_2.ReactNodeArray | React_2.ReactPortal | boolean | null | undefined | ObjectSlotProp<TProps>;

// @public (undocumented)
export type SlotPropRenderFunction<TProps> = (Component: React_2.ElementType<TProps>, props: TProps) => React_2.ReactNode;

// @public (undocumented)
export type SlotProps<TSlots extends BaseSlots, TProps, TRootProps extends React_2.HTMLAttributes<HTMLElement>> = {
    [key in keyof Omit<TSlots, 'root'>]: key extends keyof TProps ? TProps[key] : any;
} & {
    root: TRootProps;
};


// (No @packageDocumentation comment for this package)

```