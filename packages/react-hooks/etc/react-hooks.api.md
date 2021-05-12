## API Report File for "@fluentui/react-hooks"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Async } from '@fluentui/utilities';
import { ISettingsMap } from '@fluentui/utilities/lib/warn';
import { IWarnControlledUsageParams } from '@fluentui/utilities/lib/warn';
import { Point } from '@fluentui/utilities';
import * as React_2 from 'react';
import { Rectangle } from '@fluentui/utilities';

// @public (undocumented)
export type ChangeCallback<TElement extends HTMLElement, TValue, TEvent extends React_2.SyntheticEvent<TElement> | undefined> = (ev: TEvent, newValue: TValue | undefined) => void;

// @public
export interface IUseBooleanCallbacks {
    setFalse: () => void;
    setTrue: () => void;
    toggle: () => void;
}

// @public (undocumented)
export interface IWarningOptions<P> {
    conditionallyRequired?: {
        requiredProps: string[];
        conditionalPropName: string;
        condition: boolean;
    }[];
    controlledUsage?: Pick<IWarnControlledUsageParams<P>, 'valueProp' | 'defaultValueProp' | 'onChangeProp' | 'readOnlyProp'>;
    deprecations?: ISettingsMap<P>;
    mutuallyExclusive?: ISettingsMap<P>;
    name: string;
    other?: string[];
    props: P;
}

// @public
export type RefCallback<T> = ((value: T | null) => void) & React_2.RefObject<T>;

// @public
export type RefObjectFunction<T> = React_2.RefObject<T> & ((value: T) => void);

// @public (undocumented)
export type Target = Element | string | MouseEvent | Point | Rectangle | null | React_2.RefObject<Element>;

// @public
export function useAsync(): Async;

// @public
export function useBoolean(initialState: boolean): [boolean, IUseBooleanCallbacks];

// @public
export function useConst<T>(initialValue: T | (() => T)): T;

// @public @deprecated (undocumented)
export function useConstCallback<T extends (...args: any[]) => any>(callback: T): T;

// @public
export function useControllableValue<TValue, TElement extends HTMLElement>(controlledValue: TValue | undefined, defaultUncontrolledValue: TValue | undefined): Readonly<[TValue | undefined, (update: React_2.SetStateAction<TValue | undefined>) => void]>;

// @public (undocumented)
export function useControllableValue<TValue, TElement extends HTMLElement, TEvent extends React_2.SyntheticEvent<TElement> | undefined>(controlledValue: TValue | undefined, defaultUncontrolledValue: TValue | undefined, onChange: ChangeCallback<TElement, TValue, TEvent> | undefined): Readonly<[
    TValue | undefined,
    (update: React_2.SetStateAction<TValue | undefined>, ev?: React_2.FormEvent<TElement>) => void
]>;

// @public
export function useForceUpdate(): () => void;

// @public
export function useId(prefix?: string, providedId?: string): string;

// @public
export function useMergedRefs<T>(...refs: (React_2.Ref<T> | undefined)[]): RefObjectFunction<T>;

// @public
export const useMount: (callback: () => void) => void;

// @public @deprecated
export const useMountSync: (callback: () => void) => void;

// @public
export function useOnEvent<TElement extends Element, TEvent extends Event>(element: React_2.RefObject<TElement | undefined | null> | TElement | Window | Document | undefined | null, eventName: string, callback: (ev: TEvent) => void, useCapture?: boolean): void;

// @public
export function usePrevious<T>(value: T): T | undefined;

// @public
export function useRefEffect<T>(callback: (value: T) => (() => void) | void, initial?: T | null): RefCallback<T>;

// @public
export const useSetInterval: () => UseSetIntervalReturnType;

// @public (undocumented)
export type UseSetIntervalReturnType = {
    setInterval: (callback: () => void, duration: number) => number;
    clearInterval: (id: number) => void;
};

// @public
export const useSetTimeout: () => UseSetTimeoutReturnType;

// @public (undocumented)
export type UseSetTimeoutReturnType = {
    setTimeout: (callback: () => void, duration: number) => number;
    clearTimeout: (id: number) => void;
};

// @public
export function useTarget<TElement extends HTMLElement = HTMLElement>(target: Target | undefined, hostElement?: React_2.RefObject<TElement | null>): Readonly<[React_2.RefObject<Element | MouseEvent | Point | Rectangle | null>, Window | undefined]>;

// @public
export const useUnmount: (callback: () => void) => void;

// @public
export function useWarnings<P>(options: IWarningOptions<P>): void;


// (No @packageDocumentation comment for this package)

```