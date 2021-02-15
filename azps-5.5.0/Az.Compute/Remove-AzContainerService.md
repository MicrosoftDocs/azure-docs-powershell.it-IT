---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177623"
---
# <span data-ttu-id="172da-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="172da-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="172da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172da-102">SYNOPSIS</span></span>
<span data-ttu-id="172da-103">Rimuove un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="172da-103">Removes a container service.</span></span>

## <span data-ttu-id="172da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="172da-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="172da-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="172da-105">DESCRIPTION</span></span>
<span data-ttu-id="172da-106">Il cmdlet **Remove-AzContainerService** rimuove un servizio contenitore dall'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="172da-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="172da-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="172da-107">EXAMPLES</span></span>

### <span data-ttu-id="172da-108">Esempio 1: Rimuovere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="172da-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="172da-109">Questo comando rimuove il servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="172da-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="172da-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="172da-110">PARAMETERS</span></span>

### <span data-ttu-id="172da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="172da-111">-AsJob</span></span>
<span data-ttu-id="172da-112">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="172da-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="172da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172da-113">-DefaultProfile</span></span>
<span data-ttu-id="172da-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="172da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="172da-115">-Force</span><span class="sxs-lookup"><span data-stu-id="172da-115">-Force</span></span>
<span data-ttu-id="172da-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="172da-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="172da-117">-Name</span><span class="sxs-lookup"><span data-stu-id="172da-117">-Name</span></span>
<span data-ttu-id="172da-118">Specifica il nome del servizio contenitore rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172da-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="172da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172da-119">-ResourceGroupName</span></span>
<span data-ttu-id="172da-120">Specifica il gruppo di risorse del servizio contenitore rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172da-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="172da-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="172da-121">-Confirm</span></span>
<span data-ttu-id="172da-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172da-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="172da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="172da-123">-WhatIf</span></span>
<span data-ttu-id="172da-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="172da-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="172da-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="172da-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="172da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172da-126">CommonParameters</span></span>
<span data-ttu-id="172da-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172da-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="172da-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172da-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="172da-129">INPUTS</span></span>

### <span data-ttu-id="172da-130">System.String</span><span class="sxs-lookup"><span data-stu-id="172da-130">System.String</span></span>

## <span data-ttu-id="172da-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="172da-131">OUTPUTS</span></span>

### <span data-ttu-id="172da-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="172da-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="172da-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="172da-133">NOTES</span></span>

## <span data-ttu-id="172da-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="172da-134">RELATED LINKS</span></span>

[<span data-ttu-id="172da-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="172da-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="172da-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="172da-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="172da-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="172da-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


