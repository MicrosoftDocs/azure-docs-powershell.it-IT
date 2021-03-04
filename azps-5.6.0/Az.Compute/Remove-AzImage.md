---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: bcbfaefcc94415acdd1100025e1eefc2977f107a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954846"
---
# <span data-ttu-id="392ab-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="392ab-101">Remove-AzImage</span></span>

## <span data-ttu-id="392ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392ab-102">SYNOPSIS</span></span>
<span data-ttu-id="392ab-103">Rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="392ab-103">Removes an image.</span></span>

## <span data-ttu-id="392ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="392ab-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="392ab-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="392ab-105">DESCRIPTION</span></span>
<span data-ttu-id="392ab-106">Il cmdlet **Remove-AzImage** rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="392ab-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="392ab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="392ab-107">EXAMPLES</span></span>

### <span data-ttu-id="392ab-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="392ab-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="392ab-109">Questo comando rimuove l'immagine denominata 'Image01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="392ab-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="392ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="392ab-110">PARAMETERS</span></span>

### <span data-ttu-id="392ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="392ab-111">-AsJob</span></span>
<span data-ttu-id="392ab-112">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="392ab-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="392ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392ab-113">-DefaultProfile</span></span>
<span data-ttu-id="392ab-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="392ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="392ab-115">-Force</span><span class="sxs-lookup"><span data-stu-id="392ab-115">-Force</span></span>
<span data-ttu-id="392ab-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="392ab-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="392ab-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="392ab-117">-ImageName</span></span>
<span data-ttu-id="392ab-118">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="392ab-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="392ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="392ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="392ab-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="392ab-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="392ab-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="392ab-121">-Confirm</span></span>
<span data-ttu-id="392ab-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="392ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="392ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="392ab-123">-WhatIf</span></span>
<span data-ttu-id="392ab-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="392ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="392ab-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="392ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="392ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392ab-126">CommonParameters</span></span>
<span data-ttu-id="392ab-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="392ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392ab-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="392ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392ab-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="392ab-129">INPUTS</span></span>

### <span data-ttu-id="392ab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="392ab-130">System.String</span></span>

## <span data-ttu-id="392ab-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="392ab-131">OUTPUTS</span></span>

### <span data-ttu-id="392ab-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="392ab-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="392ab-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="392ab-133">NOTES</span></span>

## <span data-ttu-id="392ab-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="392ab-134">RELATED LINKS</span></span>
