---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490809"
---
# <span data-ttu-id="3e8e2-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3e8e2-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="3e8e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8e2-103">Aggiorna un servizio nella topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="3e8e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e8e2-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e8e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3e8e2-106">Il cmdlet **set-AzureRmDeploymentManagerService** aggiorna un servizio con l'oggetto servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="3e8e2-107">Il cmdlet restituisce l'oggetto servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="3e8e2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e8e2-108">EXAMPLES</span></span>

### <span data-ttu-id="3e8e2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e8e2-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="3e8e2-110">Questo comando aggiorna un servizio il cui nome, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="3e8e2-111">Il servizio verrà aggiornato alle proprietà impostate nel $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="3e8e2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e8e2-112">PARAMETERS</span></span>

### <span data-ttu-id="3e8e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8e2-113">-DefaultProfile</span></span>
<span data-ttu-id="3e8e2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8e2-115">-Servizio</span><span class="sxs-lookup"><span data-stu-id="3e8e2-115">-Service</span></span>
<span data-ttu-id="3e8e2-116">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-116">The service object.</span></span>

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

### <span data-ttu-id="3e8e2-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e8e2-117">-Confirm</span></span>
<span data-ttu-id="3e8e2-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8e2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8e2-119">-WhatIf</span></span>
<span data-ttu-id="3e8e2-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e8e2-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8e2-122">CommonParameters</span></span>
<span data-ttu-id="3e8e2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8e2-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8e2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e8e2-125">INPUTS</span></span>

### <span data-ttu-id="3e8e2-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3e8e2-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3e8e2-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e8e2-127">OUTPUTS</span></span>

### <span data-ttu-id="3e8e2-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3e8e2-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3e8e2-129">Note</span><span class="sxs-lookup"><span data-stu-id="3e8e2-129">NOTES</span></span>

## <span data-ttu-id="3e8e2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e8e2-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e8e2-131">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3e8e2-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3e8e2-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3e8e2-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3e8e2-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3e8e2-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)