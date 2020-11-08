---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029877"
---
# <span data-ttu-id="ac293-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="ac293-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="ac293-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac293-102">SYNOPSIS</span></span>
<span data-ttu-id="ac293-103">Aggiorna un'istanza di componente aggiuntivo esistente.</span><span class="sxs-lookup"><span data-stu-id="ac293-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="ac293-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac293-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ac293-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac293-105">DESCRIPTION</span></span>
<span data-ttu-id="ac293-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac293-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ac293-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ac293-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ac293-108">Questo cmdlet aggiorna un'istanza del componente aggiuntivo esistente dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ac293-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="ac293-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac293-109">EXAMPLES</span></span>

### <span data-ttu-id="ac293-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac293-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="ac293-111">Questo esempio aggiorna un componente aggiuntivo con un nuovo ID piano.</span><span class="sxs-lookup"><span data-stu-id="ac293-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="ac293-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac293-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="ac293-113">Questo esempio aggiorna un componente aggiuntivo con un nuovo ID piano e codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="ac293-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="ac293-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac293-114">PARAMETERS</span></span>

### <span data-ttu-id="ac293-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac293-115">-Name</span></span>
<span data-ttu-id="ac293-116">Specifica il nome dell'istanza del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="ac293-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="ac293-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac293-117">-PassThru</span></span>
<span data-ttu-id="ac293-118">Se specificato, il cmdlet restituisce true se il comando riesce e false se non riesce.</span><span class="sxs-lookup"><span data-stu-id="ac293-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac293-119">-Piano</span><span class="sxs-lookup"><span data-stu-id="ac293-119">-Plan</span></span>
<span data-ttu-id="ac293-120">Specifica l'ID piano.</span><span class="sxs-lookup"><span data-stu-id="ac293-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="ac293-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ac293-121">-Profile</span></span>
<span data-ttu-id="ac293-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac293-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac293-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ac293-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac293-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="ac293-124">-PromotionCode</span></span>
<span data-ttu-id="ac293-125">Specifica il codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="ac293-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="ac293-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac293-126">CommonParameters</span></span>
<span data-ttu-id="ac293-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac293-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac293-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac293-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac293-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac293-129">INPUTS</span></span>

## <span data-ttu-id="ac293-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac293-130">OUTPUTS</span></span>

## <span data-ttu-id="ac293-131">Note</span><span class="sxs-lookup"><span data-stu-id="ac293-131">NOTES</span></span>

## <span data-ttu-id="ac293-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac293-132">RELATED LINKS</span></span>

[<span data-ttu-id="ac293-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="ac293-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="ac293-134">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="ac293-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="ac293-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="ac293-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


