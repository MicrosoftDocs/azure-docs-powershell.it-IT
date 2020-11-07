---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b87c75ba197598aa3162ecb47dd81c0d003538d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675290"
---
# <span data-ttu-id="bdb48-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bdb48-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="bdb48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdb48-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb48-103">Rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="bdb48-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="bdb48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdb48-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdb48-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb48-106">Il cmdlet **Remove-AzContainerServiceAgentPoolProfile** rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="bdb48-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="bdb48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdb48-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb48-108">Esempio 1: rimuovere un profilo da un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="bdb48-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="bdb48-109">Il primo comando ottiene un servizio contenitore denominato CSResourceGroup17 tramite il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="bdb48-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="bdb48-110">Il comando Archivia il servizio nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="bdb48-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="bdb48-111">Il secondo comando rimuove il profilo denominato AgentPool01 dal servizio contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="bdb48-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="bdb48-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdb48-112">PARAMETERS</span></span>

### <span data-ttu-id="bdb48-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="bdb48-113">-ContainerService</span></span>
<span data-ttu-id="bdb48-114">Specifica l'oggetto servizio contenitore da cui questo cmdlet rimuove un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="bdb48-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="bdb48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb48-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb48-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb48-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdb48-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdb48-117">-Name</span></span>
<span data-ttu-id="bdb48-118">Specifica il nome del profilo del pool di agenti rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb48-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdb48-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdb48-119">-Confirm</span></span>
<span data-ttu-id="bdb48-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb48-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb48-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb48-121">-WhatIf</span></span>
<span data-ttu-id="bdb48-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdb48-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdb48-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdb48-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb48-124">CommonParameters</span></span>
<span data-ttu-id="bdb48-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb48-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb48-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb48-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdb48-127">INPUTS</span></span>

### <span data-ttu-id="bdb48-128">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="bdb48-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="bdb48-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bdb48-129">System.String</span></span>

## <span data-ttu-id="bdb48-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdb48-130">OUTPUTS</span></span>

### <span data-ttu-id="bdb48-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="bdb48-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="bdb48-132">Note</span><span class="sxs-lookup"><span data-stu-id="bdb48-132">NOTES</span></span>

## <span data-ttu-id="bdb48-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdb48-133">RELATED LINKS</span></span>

[<span data-ttu-id="bdb48-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bdb48-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="bdb48-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="bdb48-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


