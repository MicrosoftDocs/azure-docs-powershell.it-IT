---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196502"
---
# <span data-ttu-id="23036-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="23036-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="23036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23036-102">SYNOPSIS</span></span>
<span data-ttu-id="23036-103">Aggiorna la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="23036-103">Updates the service topology.</span></span>

## <span data-ttu-id="23036-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23036-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23036-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="23036-105">DESCRIPTION</span></span>
<span data-ttu-id="23036-106">Il cmdlet **Set-AzDeploymentManagerServiceTopology** aggiorna una topologia di servizio con l'oggetto topologia di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="23036-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="23036-107">Il cmdlet restituisce l'oggetto topologia del servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="23036-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="23036-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23036-108">EXAMPLES</span></span>

### <span data-ttu-id="23036-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23036-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="23036-110">Questo comando aggiorna una topologia di servizio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName del $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="23036-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="23036-111">Il comando restituisce l'oggetto topologia di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="23036-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="23036-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23036-112">PARAMETERS</span></span>

### <span data-ttu-id="23036-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23036-113">-DefaultProfile</span></span>
<span data-ttu-id="23036-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23036-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23036-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23036-115">-InputObject</span></span>
<span data-ttu-id="23036-116">Oggetto topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="23036-116">The service topology object.</span></span>

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

### <span data-ttu-id="23036-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23036-117">-Confirm</span></span>
<span data-ttu-id="23036-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23036-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23036-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23036-119">-WhatIf</span></span>
<span data-ttu-id="23036-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23036-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23036-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23036-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23036-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23036-122">CommonParameters</span></span>
<span data-ttu-id="23036-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23036-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23036-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23036-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23036-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="23036-125">INPUTS</span></span>

### <span data-ttu-id="23036-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="23036-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="23036-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23036-127">OUTPUTS</span></span>

### <span data-ttu-id="23036-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="23036-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="23036-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="23036-129">NOTES</span></span>

## <span data-ttu-id="23036-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23036-130">RELATED LINKS</span></span>
