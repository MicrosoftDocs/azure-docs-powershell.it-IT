---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031584"
---
# <span data-ttu-id="afdd0-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="afdd0-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="afdd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="afdd0-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="afdd0-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="afdd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afdd0-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afdd0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afdd0-105">DESCRIPTION</span></span>
<span data-ttu-id="afdd0-106">Il cmdlet **Remove-AzAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="afdd0-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="afdd0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afdd0-107">EXAMPLES</span></span>

### <span data-ttu-id="afdd0-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="afdd0-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="afdd0-109">Questo comando rimuove un set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="afdd0-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="afdd0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afdd0-110">PARAMETERS</span></span>

### <span data-ttu-id="afdd0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afdd0-111">-AsJob</span></span>
<span data-ttu-id="afdd0-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="afdd0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdd0-113">-DefaultProfile</span></span>
<span data-ttu-id="afdd0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afdd0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="afdd0-115">-Force</span></span>
<span data-ttu-id="afdd0-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="afdd0-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="afdd0-117">-Name</span></span>
<span data-ttu-id="afdd0-118">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="afdd0-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afdd0-119">-ResourceGroupName</span></span>
<span data-ttu-id="afdd0-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="afdd0-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="afdd0-121">-Confirm</span></span>
<span data-ttu-id="afdd0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afdd0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdd0-123">-WhatIf</span></span>
<span data-ttu-id="afdd0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afdd0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afdd0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afdd0-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdd0-126">CommonParameters</span></span>
<span data-ttu-id="afdd0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdd0-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afdd0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdd0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afdd0-129">INPUTS</span></span>

### <span data-ttu-id="afdd0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="afdd0-130">System.String</span></span>

## <span data-ttu-id="afdd0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afdd0-131">OUTPUTS</span></span>

### <span data-ttu-id="afdd0-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="afdd0-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="afdd0-133">Note</span><span class="sxs-lookup"><span data-stu-id="afdd0-133">NOTES</span></span>

## <span data-ttu-id="afdd0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afdd0-134">RELATED LINKS</span></span>

[<span data-ttu-id="afdd0-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="afdd0-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="afdd0-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="afdd0-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


