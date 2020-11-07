---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 28dc0bd04484823636398b828922fbb79db24672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674595"
---
# <span data-ttu-id="3096a-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3096a-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="3096a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3096a-102">SYNOPSIS</span></span>
<span data-ttu-id="3096a-103">Aggiorna il servizio.</span><span class="sxs-lookup"><span data-stu-id="3096a-103">Updates the service.</span></span>

## <span data-ttu-id="3096a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3096a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3096a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3096a-105">DESCRIPTION</span></span>
<span data-ttu-id="3096a-106">Il cmdlet **set-AzDeploymentManagerService** aggiorna un servizio con l'oggetto servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="3096a-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="3096a-107">Il cmdlet restituisce l'oggetto servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3096a-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="3096a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3096a-108">EXAMPLES</span></span>

### <span data-ttu-id="3096a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3096a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="3096a-110">Questo comando aggiorna un servizio il cui nome, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3096a-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="3096a-111">Il servizio verrà aggiornato alle proprietà impostate nel $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3096a-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="3096a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3096a-112">PARAMETERS</span></span>

### <span data-ttu-id="3096a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3096a-113">-DefaultProfile</span></span>
<span data-ttu-id="3096a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3096a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3096a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3096a-115">-InputObject</span></span>
<span data-ttu-id="3096a-116">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="3096a-116">The service object.</span></span>

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

### <span data-ttu-id="3096a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3096a-117">-Confirm</span></span>
<span data-ttu-id="3096a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3096a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3096a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3096a-119">-WhatIf</span></span>
<span data-ttu-id="3096a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3096a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3096a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3096a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3096a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3096a-122">CommonParameters</span></span>
<span data-ttu-id="3096a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3096a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3096a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3096a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3096a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3096a-125">INPUTS</span></span>

### <span data-ttu-id="3096a-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3096a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3096a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3096a-127">OUTPUTS</span></span>

### <span data-ttu-id="3096a-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3096a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3096a-129">Note</span><span class="sxs-lookup"><span data-stu-id="3096a-129">NOTES</span></span>

## <span data-ttu-id="3096a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3096a-130">RELATED LINKS</span></span>