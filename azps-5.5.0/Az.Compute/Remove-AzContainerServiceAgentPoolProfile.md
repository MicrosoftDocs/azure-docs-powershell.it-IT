---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210026"
---
# <span data-ttu-id="d4a89-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d4a89-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="d4a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a89-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a89-103">Rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d4a89-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="d4a89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4a89-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a89-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4a89-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a89-106">Il cmdlet **Remove-AzContainerServiceAgentPoolProfile** rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d4a89-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="d4a89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4a89-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a89-108">Esempio 1: Rimuovere un profilo da un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="d4a89-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="d4a89-109">Il primo comando ottiene un servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="d4a89-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="d4a89-110">Il comando archivia il servizio nella variabile $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="d4a89-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="d4a89-111">Il secondo comando rimuove il profilo denominato AgentPool01 dal servizio contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="d4a89-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="d4a89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4a89-112">PARAMETERS</span></span>

### <span data-ttu-id="d4a89-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="d4a89-113">-ContainerService</span></span>
<span data-ttu-id="d4a89-114">Specifica l'oggetto servizio contenitore da cui questo cmdlet rimuove un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="d4a89-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a89-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a89-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a89-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a89-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d4a89-117">-Name</span></span>
<span data-ttu-id="d4a89-118">Specifica il nome del profilo del pool di agenti rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a89-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d4a89-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4a89-119">-Confirm</span></span>
<span data-ttu-id="d4a89-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a89-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a89-121">-WhatIf</span></span>
<span data-ttu-id="d4a89-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4a89-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4a89-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4a89-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a89-124">CommonParameters</span></span>
<span data-ttu-id="d4a89-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a89-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4a89-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a89-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4a89-127">INPUTS</span></span>

### <span data-ttu-id="d4a89-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d4a89-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="d4a89-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d4a89-129">System.String</span></span>

## <span data-ttu-id="d4a89-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4a89-130">OUTPUTS</span></span>

### <span data-ttu-id="d4a89-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d4a89-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d4a89-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4a89-132">NOTES</span></span>

## <span data-ttu-id="d4a89-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4a89-133">RELATED LINKS</span></span>

[<span data-ttu-id="d4a89-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d4a89-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d4a89-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d4a89-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


