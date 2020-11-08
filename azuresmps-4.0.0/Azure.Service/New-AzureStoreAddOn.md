---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029663"
---
# <span data-ttu-id="a9121-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9121-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="a9121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9121-102">SYNOPSIS</span></span>
<span data-ttu-id="a9121-103">Acquista una nuova istanza del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9121-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="a9121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9121-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a9121-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9121-105">DESCRIPTION</span></span>
<span data-ttu-id="a9121-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a9121-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a9121-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a9121-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a9121-108">Acquista una nuova istanza del componente aggiuntivo da Azure Store.</span><span class="sxs-lookup"><span data-stu-id="a9121-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="a9121-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9121-109">EXAMPLES</span></span>

### <span data-ttu-id="a9121-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9121-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="a9121-111">In questo esempio viene acquistato un componente aggiuntivo denominato AddOn con un PlanId nella posizione West US.</span><span class="sxs-lookup"><span data-stu-id="a9121-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="a9121-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a9121-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="a9121-113">Questo esempio usa un codice promozionale per acquistare un componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9121-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="a9121-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9121-114">PARAMETERS</span></span>

### <span data-ttu-id="a9121-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="a9121-115">-AddOn</span></span>
<span data-ttu-id="a9121-116">Specifica l'ID del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9121-116">Specifies the add-on ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9121-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a9121-117">-Location</span></span>
<span data-ttu-id="a9121-118">Specifica il percorso dell'istanza del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9121-118">Specifies the add-on instance location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9121-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9121-119">-Name</span></span>
<span data-ttu-id="a9121-120">Specifica il nome dell'istanza del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9121-120">Specifies the name of the add-on instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9121-121">-Piano</span><span class="sxs-lookup"><span data-stu-id="a9121-121">-Plan</span></span>
<span data-ttu-id="a9121-122">Specifica l'ID piano.</span><span class="sxs-lookup"><span data-stu-id="a9121-122">Specifies the plan ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9121-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9121-123">-Profile</span></span>
<span data-ttu-id="a9121-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9121-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9121-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a9121-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9121-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="a9121-126">-PromotionCode</span></span>
<span data-ttu-id="a9121-127">Specifica un codice promozionale da applicare all'acquisto.</span><span class="sxs-lookup"><span data-stu-id="a9121-127">Specifies a promotion code to apply to the purchase.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9121-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9121-128">CommonParameters</span></span>
<span data-ttu-id="a9121-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9121-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9121-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9121-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9121-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9121-131">INPUTS</span></span>

## <span data-ttu-id="a9121-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9121-132">OUTPUTS</span></span>

## <span data-ttu-id="a9121-133">Note</span><span class="sxs-lookup"><span data-stu-id="a9121-133">NOTES</span></span>

## <span data-ttu-id="a9121-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9121-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9121-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9121-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="a9121-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9121-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="a9121-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9121-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


