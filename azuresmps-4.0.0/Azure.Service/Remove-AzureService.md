---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029589"
---
# <span data-ttu-id="cd649-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="cd649-101">Remove-AzureService</span></span>

## <span data-ttu-id="cd649-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd649-102">SYNOPSIS</span></span>
<span data-ttu-id="cd649-103">Rimuove il servizio Cloud corrente.</span><span class="sxs-lookup"><span data-stu-id="cd649-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="cd649-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd649-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd649-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd649-105">DESCRIPTION</span></span>
<span data-ttu-id="cd649-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd649-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cd649-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cd649-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cd649-108">Il cmdlet **Remove-AzureService** arresta e rimuove il servizio Cloud corrente oppure il servizio che corrisponde al nome del servizio e dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="cd649-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="cd649-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd649-109">EXAMPLES</span></span>

## <span data-ttu-id="cd649-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd649-110">PARAMETERS</span></span>

### <span data-ttu-id="cd649-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="cd649-111">-DeleteAll</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd649-112">-Force</span><span class="sxs-lookup"><span data-stu-id="cd649-112">-Force</span></span>
<span data-ttu-id="cd649-113">Rimuove il servizio senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cd649-113">Removes the service without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd649-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd649-114">-PassThru</span></span>
<span data-ttu-id="cd649-115">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cd649-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd649-116">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cd649-116">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd649-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="cd649-117">-Profile</span></span>
<span data-ttu-id="cd649-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd649-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd649-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cd649-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd649-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd649-120">-ServiceName</span></span>
<span data-ttu-id="cd649-121">Specifica il nome del servizio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cd649-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="cd649-122">Se il comando viene eseguito da una directory del servizio e non viene specificato alcun nome, viene usato il nome del servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="cd649-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

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

### <span data-ttu-id="cd649-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd649-123">-Confirm</span></span>
<span data-ttu-id="cd649-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd649-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd649-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd649-125">-WhatIf</span></span>
<span data-ttu-id="cd649-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd649-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd649-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd649-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd649-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd649-128">CommonParameters</span></span>
<span data-ttu-id="cd649-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd649-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd649-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd649-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd649-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd649-131">INPUTS</span></span>

## <span data-ttu-id="cd649-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd649-132">OUTPUTS</span></span>

## <span data-ttu-id="cd649-133">Note</span><span class="sxs-lookup"><span data-stu-id="cd649-133">NOTES</span></span>

## <span data-ttu-id="cd649-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd649-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd649-135">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="cd649-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="cd649-136">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="cd649-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="cd649-137">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="cd649-137">Start-AzureService</span></span>](./Start-AzureService.md)


