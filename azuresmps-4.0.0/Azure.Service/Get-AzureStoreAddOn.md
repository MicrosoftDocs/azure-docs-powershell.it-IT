---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023505"
---
# <span data-ttu-id="834c5-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="834c5-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="834c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="834c5-102">SYNOPSIS</span></span>
<span data-ttu-id="834c5-103">Ottiene i componenti aggiuntivi di Azure Store disponibili.</span><span class="sxs-lookup"><span data-stu-id="834c5-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="834c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="834c5-104">SYNTAX</span></span>

### <span data-ttu-id="834c5-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="834c5-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="834c5-106">Getaddon</span><span class="sxs-lookup"><span data-stu-id="834c5-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="834c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="834c5-107">DESCRIPTION</span></span>
<span data-ttu-id="834c5-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="834c5-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="834c5-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="834c5-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="834c5-110">Ottiene tutti i componenti aggiuntivi disponibili per l'acquisto da Azure Store oppure ottiene le istanze del componente aggiuntivo esistenti per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="834c5-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="834c5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="834c5-111">EXAMPLES</span></span>

### <span data-ttu-id="834c5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="834c5-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="834c5-113">Questo esempio consente di ottenere tutte le istanze del componente aggiuntivo acquistate per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="834c5-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="834c5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="834c5-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="834c5-115">Questo esempio consente di ottenere tutti i componenti aggiuntivi disponibili per l'acquisto in Stati Uniti da Azure Store.</span><span class="sxs-lookup"><span data-stu-id="834c5-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="834c5-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="834c5-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="834c5-117">Questo esempio ottiene un componente aggiuntivo denominato AddOn dall'istanza del componente aggiuntivo acquistata nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="834c5-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="834c5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="834c5-118">PARAMETERS</span></span>

### <span data-ttu-id="834c5-119">-Paese</span><span class="sxs-lookup"><span data-stu-id="834c5-119">-Country</span></span>
<span data-ttu-id="834c5-120">Se specificato, restituisce solo le istanze del componente aggiuntivo Azure Store disponibili nel paese specificato.</span><span class="sxs-lookup"><span data-stu-id="834c5-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="834c5-121">Il valore predefinito è "US".</span><span class="sxs-lookup"><span data-stu-id="834c5-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="834c5-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="834c5-122">-ListAvailable</span></span>
<span data-ttu-id="834c5-123">Se specificato, ottiene i componenti aggiuntivi disponibili per l'acquisto da Azure Store.</span><span class="sxs-lookup"><span data-stu-id="834c5-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="834c5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="834c5-124">-Name</span></span>
<span data-ttu-id="834c5-125">Restituisce il componente aggiuntivo che corrisponde al nome specificato.</span><span class="sxs-lookup"><span data-stu-id="834c5-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="834c5-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="834c5-126">-Profile</span></span>
<span data-ttu-id="834c5-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="834c5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="834c5-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="834c5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="834c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="834c5-129">CommonParameters</span></span>
<span data-ttu-id="834c5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="834c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="834c5-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="834c5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="834c5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="834c5-132">INPUTS</span></span>

## <span data-ttu-id="834c5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="834c5-133">OUTPUTS</span></span>

## <span data-ttu-id="834c5-134">Note</span><span class="sxs-lookup"><span data-stu-id="834c5-134">NOTES</span></span>

## <span data-ttu-id="834c5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="834c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="834c5-136">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="834c5-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="834c5-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="834c5-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="834c5-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="834c5-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


