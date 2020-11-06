---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509980"
---
# <span data-ttu-id="93e60-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93e60-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="93e60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93e60-102">SYNOPSIS</span></span>
<span data-ttu-id="93e60-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="93e60-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93e60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93e60-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93e60-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93e60-105">DESCRIPTION</span></span>
<span data-ttu-id="93e60-106">Il cmdlet **Remove-AzureRmAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="93e60-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="93e60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93e60-107">EXAMPLES</span></span>

### <span data-ttu-id="93e60-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="93e60-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="93e60-109">Questo comando rimuove un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93e60-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="93e60-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93e60-110">PARAMETERS</span></span>

### <span data-ttu-id="93e60-111">-Force</span><span class="sxs-lookup"><span data-stu-id="93e60-111">-Force</span></span>
<span data-ttu-id="93e60-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="93e60-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e60-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="93e60-113">-Name</span></span>
<span data-ttu-id="93e60-114">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="93e60-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e60-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e60-115">-ResourceGroupName</span></span>
<span data-ttu-id="93e60-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93e60-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e60-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93e60-117">-Confirm</span></span>
<span data-ttu-id="93e60-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e60-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e60-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e60-119">-WhatIf</span></span>
<span data-ttu-id="93e60-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93e60-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="93e60-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93e60-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e60-122">CommonParameters</span></span>
<span data-ttu-id="93e60-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e60-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e60-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e60-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93e60-125">INPUTS</span></span>

### <span data-ttu-id="93e60-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="93e60-126">None</span></span>
<span data-ttu-id="93e60-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="93e60-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93e60-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93e60-128">OUTPUTS</span></span>

## <span data-ttu-id="93e60-129">Note</span><span class="sxs-lookup"><span data-stu-id="93e60-129">NOTES</span></span>

## <span data-ttu-id="93e60-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93e60-130">RELATED LINKS</span></span>

[<span data-ttu-id="93e60-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93e60-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="93e60-132">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93e60-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


