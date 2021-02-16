---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204850"
---
# <span data-ttu-id="251a6-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="251a6-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="251a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="251a6-102">SYNOPSIS</span></span>
<span data-ttu-id="251a6-103">Rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="251a6-103">Removes a snapshot.</span></span>

## <span data-ttu-id="251a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="251a6-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="251a6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="251a6-105">DESCRIPTION</span></span>
<span data-ttu-id="251a6-106">Il cmdlet **Remove-AzSnapshot** rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="251a6-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="251a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="251a6-107">EXAMPLES</span></span>

### <span data-ttu-id="251a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="251a6-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="251a6-109">Questo comando rimuove lo snapshot denominato 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="251a6-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="251a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="251a6-110">PARAMETERS</span></span>

### <span data-ttu-id="251a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="251a6-111">-AsJob</span></span>
<span data-ttu-id="251a6-112">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="251a6-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="251a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251a6-113">-DefaultProfile</span></span>
<span data-ttu-id="251a6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="251a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="251a6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="251a6-115">-Force</span></span>
<span data-ttu-id="251a6-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="251a6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="251a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="251a6-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="251a6-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="251a6-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="251a6-119">-SnapshotName</span></span>
<span data-ttu-id="251a6-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="251a6-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="251a6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="251a6-121">-Confirm</span></span>
<span data-ttu-id="251a6-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="251a6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251a6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251a6-123">-WhatIf</span></span>
<span data-ttu-id="251a6-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="251a6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="251a6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="251a6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251a6-126">CommonParameters</span></span>
<span data-ttu-id="251a6-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="251a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251a6-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="251a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251a6-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="251a6-129">INPUTS</span></span>

### <span data-ttu-id="251a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="251a6-130">System.String</span></span>

## <span data-ttu-id="251a6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="251a6-131">OUTPUTS</span></span>

### <span data-ttu-id="251a6-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="251a6-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="251a6-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="251a6-133">NOTES</span></span>

## <span data-ttu-id="251a6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="251a6-134">RELATED LINKS</span></span>
