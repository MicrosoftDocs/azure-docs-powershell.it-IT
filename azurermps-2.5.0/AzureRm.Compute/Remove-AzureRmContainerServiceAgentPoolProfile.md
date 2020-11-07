---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866729"
---
# <span data-ttu-id="e2982-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e2982-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="e2982-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2982-102">SYNOPSIS</span></span>
<span data-ttu-id="e2982-103">Rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2982-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2982-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2982-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2982-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2982-105">DESCRIPTION</span></span>
<span data-ttu-id="e2982-106">Il cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2982-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="e2982-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2982-107">EXAMPLES</span></span>

### <span data-ttu-id="e2982-108">Esempio 1: rimuovere un profilo da un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="e2982-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="e2982-109">Il primo comando ottiene un servizio contenitore denominato CSResourceGroup17 tramite il cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="e2982-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="e2982-110">Il comando Archivia il servizio nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="e2982-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="e2982-111">Il secondo comando rimuove il profilo denominato AgentPool01 dal servizio contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="e2982-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="e2982-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2982-112">PARAMETERS</span></span>

### <span data-ttu-id="e2982-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e2982-113">-ContainerService</span></span>
<span data-ttu-id="e2982-114">Specifica l'oggetto servizio contenitore da cui questo cmdlet rimuove un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="e2982-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="e2982-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2982-115">-DefaultProfile</span></span>
<span data-ttu-id="e2982-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2982-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2982-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2982-117">-Name</span></span>
<span data-ttu-id="e2982-118">Specifica il nome del profilo del pool di agenti rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2982-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2982-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2982-119">-Confirm</span></span>
<span data-ttu-id="e2982-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2982-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2982-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2982-121">-WhatIf</span></span>
<span data-ttu-id="e2982-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2982-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2982-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2982-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2982-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2982-124">CommonParameters</span></span>
<span data-ttu-id="e2982-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2982-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2982-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2982-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2982-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2982-127">INPUTS</span></span>

### <span data-ttu-id="e2982-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="e2982-128">ContainerService</span></span>
<span data-ttu-id="e2982-129">Il parametro ' ContainerService ' accetta il valore di tipo ' ContainerService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e2982-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="e2982-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2982-130">OUTPUTS</span></span>

### <span data-ttu-id="e2982-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e2982-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e2982-132">Note</span><span class="sxs-lookup"><span data-stu-id="e2982-132">NOTES</span></span>

## <span data-ttu-id="e2982-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2982-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2982-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e2982-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e2982-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e2982-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


