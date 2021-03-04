---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7e3ed99abe5fb7a679506571d7d734cad02084d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966253"
---
# <span data-ttu-id="0f7c9-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0f7c9-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="0f7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7c9-103">Aggiorna la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-103">Updates the service topology.</span></span>

## <span data-ttu-id="0f7c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f7c9-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f7c9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="0f7c9-106">Il cmdlet **Set-AzDeploymentManagerServiceTopology** aggiorna la topologia di un servizio con l'oggetto topologia di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="0f7c9-107">Il cmdlet restituisce l'oggetto topologia del servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="0f7c9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f7c9-108">EXAMPLES</span></span>

### <span data-ttu-id="0f7c9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f7c9-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="0f7c9-110">Questo comando aggiorna una topologia di servizio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName del $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="0f7c9-111">Il comando restituisce l'oggetto topologia del servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="0f7c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f7c9-112">PARAMETERS</span></span>

### <span data-ttu-id="0f7c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7c9-113">-DefaultProfile</span></span>
<span data-ttu-id="0f7c9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f7c9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f7c9-115">-InputObject</span></span>
<span data-ttu-id="0f7c9-116">Oggetto topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-116">The service topology object.</span></span>

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

### <span data-ttu-id="0f7c9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f7c9-117">-Confirm</span></span>
<span data-ttu-id="0f7c9-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f7c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7c9-119">-WhatIf</span></span>
<span data-ttu-id="0f7c9-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f7c9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f7c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7c9-122">CommonParameters</span></span>
<span data-ttu-id="0f7c9-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7c9-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f7c9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7c9-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f7c9-125">INPUTS</span></span>

### <span data-ttu-id="0f7c9-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="0f7c9-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="0f7c9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f7c9-127">OUTPUTS</span></span>

### <span data-ttu-id="0f7c9-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="0f7c9-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="0f7c9-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f7c9-129">NOTES</span></span>

## <span data-ttu-id="0f7c9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f7c9-130">RELATED LINKS</span></span>
