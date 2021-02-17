---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196510"
---
# <span data-ttu-id="bc06d-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="bc06d-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="bc06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc06d-102">SYNOPSIS</span></span>
<span data-ttu-id="bc06d-103">Aggiorna il servizio.</span><span class="sxs-lookup"><span data-stu-id="bc06d-103">Updates the service.</span></span>

## <span data-ttu-id="bc06d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc06d-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc06d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc06d-105">DESCRIPTION</span></span>
<span data-ttu-id="bc06d-106">Il cmdlet **Set-AzDeploymentManagerService** aggiorna un servizio con l'oggetto servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="bc06d-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="bc06d-107">Il cmdlet restituisce l'oggetto servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bc06d-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="bc06d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc06d-108">EXAMPLES</span></span>

### <span data-ttu-id="bc06d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc06d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="bc06d-110">Questo comando aggiorna un servizio il cui nome, il cui nome della topologia di servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName del $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="bc06d-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="bc06d-111">Il servizio verrà aggiornato alle proprietà impostate nel $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="bc06d-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="bc06d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc06d-112">PARAMETERS</span></span>

### <span data-ttu-id="bc06d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc06d-113">-DefaultProfile</span></span>
<span data-ttu-id="bc06d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc06d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc06d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc06d-115">-InputObject</span></span>
<span data-ttu-id="bc06d-116">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="bc06d-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc06d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc06d-117">-Confirm</span></span>
<span data-ttu-id="bc06d-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc06d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc06d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc06d-119">-WhatIf</span></span>
<span data-ttu-id="bc06d-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc06d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc06d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc06d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc06d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc06d-122">CommonParameters</span></span>
<span data-ttu-id="bc06d-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc06d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc06d-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc06d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc06d-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc06d-125">INPUTS</span></span>

### <span data-ttu-id="bc06d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="bc06d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="bc06d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc06d-127">OUTPUTS</span></span>

### <span data-ttu-id="bc06d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="bc06d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="bc06d-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc06d-129">NOTES</span></span>

## <span data-ttu-id="bc06d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc06d-130">RELATED LINKS</span></span>
