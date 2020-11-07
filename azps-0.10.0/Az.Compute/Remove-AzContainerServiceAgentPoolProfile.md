---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 75e019b9c60a45c1bed8e830d9810b1c6a58e732
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863578"
---
# <span data-ttu-id="1fc2a-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1fc2a-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="1fc2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc2a-103">Rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="1fc2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fc2a-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fc2a-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc2a-106">Il cmdlet **Remove-AzContainerServiceAgentPoolProfile** rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="1fc2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fc2a-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc2a-108">Esempio 1: rimuovere un profilo da un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="1fc2a-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="1fc2a-109">Il primo comando ottiene un servizio contenitore denominato CSResourceGroup17 tramite il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="1fc2a-110">Il comando Archivia il servizio nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="1fc2a-111">Il secondo comando rimuove il profilo denominato AgentPool01 dal servizio contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="1fc2a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fc2a-112">PARAMETERS</span></span>

### <span data-ttu-id="1fc2a-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1fc2a-113">-ContainerService</span></span>
<span data-ttu-id="1fc2a-114">Specifica l'oggetto servizio contenitore da cui questo cmdlet rimuove un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc2a-115">-DefaultProfile</span></span>
<span data-ttu-id="1fc2a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc2a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fc2a-117">-Name</span></span>
<span data-ttu-id="1fc2a-118">Specifica il nome del profilo del pool di agenti rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc2a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fc2a-119">-Confirm</span></span>
<span data-ttu-id="1fc2a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc2a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc2a-121">-WhatIf</span></span>
<span data-ttu-id="1fc2a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fc2a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc2a-124">CommonParameters</span></span>
<span data-ttu-id="1fc2a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc2a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc2a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc2a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fc2a-127">INPUTS</span></span>

### <span data-ttu-id="1fc2a-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="1fc2a-128">ContainerService</span></span>
<span data-ttu-id="1fc2a-129">Il parametro ' ContainerService ' accetta il valore di tipo ' ContainerService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1fc2a-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="1fc2a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fc2a-130">OUTPUTS</span></span>

### <span data-ttu-id="1fc2a-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1fc2a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1fc2a-132">Note</span><span class="sxs-lookup"><span data-stu-id="1fc2a-132">NOTES</span></span>

## <span data-ttu-id="1fc2a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fc2a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1fc2a-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1fc2a-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="1fc2a-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1fc2a-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


