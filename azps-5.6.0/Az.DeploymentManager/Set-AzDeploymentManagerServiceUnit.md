---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 24c682faf725fd53e3b78e85c316318300ecbb62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962093"
---
# <span data-ttu-id="429ec-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="429ec-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="429ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="429ec-102">SYNOPSIS</span></span>
<span data-ttu-id="429ec-103">Aggiorna l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="429ec-103">Updates the service unit.</span></span>

## <span data-ttu-id="429ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="429ec-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="429ec-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="429ec-105">DESCRIPTION</span></span>
<span data-ttu-id="429ec-106">Il cmdlet **Set-AzDeploymentManagerServiceUnit** aggiorna un'unità di servizio con l'oggetto unità di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="429ec-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="429ec-107">Il cmdlet restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="429ec-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="429ec-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="429ec-108">EXAMPLES</span></span>

### <span data-ttu-id="429ec-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="429ec-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="429ec-110">Questo comando aggiorna un'unità di servizio il cui nome, nome del servizio, nome della topologia di servizio e Gruppo Di risorse corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName del $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="429ec-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="429ec-111">Il comando restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="429ec-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="429ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="429ec-112">PARAMETERS</span></span>

### <span data-ttu-id="429ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429ec-113">-DefaultProfile</span></span>
<span data-ttu-id="429ec-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="429ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="429ec-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="429ec-115">-InputObject</span></span>
<span data-ttu-id="429ec-116">Oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="429ec-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="429ec-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="429ec-117">-Confirm</span></span>
<span data-ttu-id="429ec-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429ec-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="429ec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="429ec-119">-WhatIf</span></span>
<span data-ttu-id="429ec-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="429ec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="429ec-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="429ec-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="429ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429ec-122">CommonParameters</span></span>
<span data-ttu-id="429ec-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429ec-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="429ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429ec-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="429ec-125">INPUTS</span></span>

### <span data-ttu-id="429ec-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="429ec-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="429ec-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="429ec-127">OUTPUTS</span></span>

### <span data-ttu-id="429ec-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="429ec-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="429ec-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="429ec-129">NOTES</span></span>

## <span data-ttu-id="429ec-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="429ec-130">RELATED LINKS</span></span>
