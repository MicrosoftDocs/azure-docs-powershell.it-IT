---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 7dccf9410ff4d03503763354aabbe6b02d0c0c6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675294"
---
# <span data-ttu-id="66a9e-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66a9e-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="66a9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="66a9e-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="66a9e-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="66a9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66a9e-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="66a9e-106">Il cmdlet **Remove-AzAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="66a9e-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="66a9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="66a9e-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="66a9e-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="66a9e-109">Questo comando rimuove un set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="66a9e-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="66a9e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66a9e-110">PARAMETERS</span></span>

### <span data-ttu-id="66a9e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66a9e-111">-AsJob</span></span>
<span data-ttu-id="66a9e-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="66a9e-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="66a9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a9e-113">-DefaultProfile</span></span>
<span data-ttu-id="66a9e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66a9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a9e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="66a9e-115">-Force</span></span>
<span data-ttu-id="66a9e-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66a9e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66a9e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="66a9e-117">-Name</span></span>
<span data-ttu-id="66a9e-118">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="66a9e-118">The availability set name.</span></span>

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

### <span data-ttu-id="66a9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="66a9e-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66a9e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="66a9e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66a9e-121">-Confirm</span></span>
<span data-ttu-id="66a9e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a9e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a9e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a9e-123">-WhatIf</span></span>
<span data-ttu-id="66a9e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a9e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a9e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a9e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a9e-126">CommonParameters</span></span>
<span data-ttu-id="66a9e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a9e-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66a9e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a9e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66a9e-129">INPUTS</span></span>

### <span data-ttu-id="66a9e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="66a9e-130">System.String</span></span>

## <span data-ttu-id="66a9e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66a9e-131">OUTPUTS</span></span>

### <span data-ttu-id="66a9e-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="66a9e-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="66a9e-133">Note</span><span class="sxs-lookup"><span data-stu-id="66a9e-133">NOTES</span></span>

## <span data-ttu-id="66a9e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66a9e-134">RELATED LINKS</span></span>

[<span data-ttu-id="66a9e-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66a9e-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="66a9e-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66a9e-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

