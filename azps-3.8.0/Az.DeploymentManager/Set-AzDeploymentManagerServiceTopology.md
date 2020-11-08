---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022320"
---
# <span data-ttu-id="f438c-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="f438c-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="f438c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f438c-102">SYNOPSIS</span></span>
<span data-ttu-id="f438c-103">Aggiorna la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="f438c-103">Updates the service topology.</span></span>

## <span data-ttu-id="f438c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f438c-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f438c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f438c-105">DESCRIPTION</span></span>
<span data-ttu-id="f438c-106">Il cmdlet **set-AzDeploymentManagerServiceTopology** aggiorna una topologia di servizio con l'oggetto topologia di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="f438c-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="f438c-107">Il cmdlet restituisce l'oggetto della topologia del servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f438c-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="f438c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f438c-108">EXAMPLES</span></span>

### <span data-ttu-id="f438c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f438c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="f438c-110">Questo comando aggiorna una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="f438c-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="f438c-111">Il comando restituisce l'oggetto della topologia del servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f438c-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="f438c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f438c-112">PARAMETERS</span></span>

### <span data-ttu-id="f438c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f438c-113">-DefaultProfile</span></span>
<span data-ttu-id="f438c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f438c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f438c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f438c-115">-InputObject</span></span>
<span data-ttu-id="f438c-116">Oggetto topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="f438c-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f438c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f438c-117">-Confirm</span></span>
<span data-ttu-id="f438c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f438c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f438c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f438c-119">-WhatIf</span></span>
<span data-ttu-id="f438c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f438c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f438c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f438c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f438c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f438c-122">CommonParameters</span></span>
<span data-ttu-id="f438c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f438c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f438c-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f438c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f438c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f438c-125">INPUTS</span></span>

### <span data-ttu-id="f438c-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="f438c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="f438c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f438c-127">OUTPUTS</span></span>

### <span data-ttu-id="f438c-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="f438c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="f438c-129">Note</span><span class="sxs-lookup"><span data-stu-id="f438c-129">NOTES</span></span>

## <span data-ttu-id="f438c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f438c-130">RELATED LINKS</span></span>
