---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3509212801aaeda9926b7f441e0aae7e17f8cbb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674589"
---
# <span data-ttu-id="c2315-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c2315-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c2315-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2315-102">SYNOPSIS</span></span>
<span data-ttu-id="c2315-103">Aggiorna l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c2315-103">Updates the service unit.</span></span>

## <span data-ttu-id="c2315-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2315-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2315-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2315-105">DESCRIPTION</span></span>
<span data-ttu-id="c2315-106">Il cmdlet **set-AzDeploymentManagerServiceUnit** aggiorna un'unità di servizio con l'oggetto unità di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="c2315-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="c2315-107">Il cmdlet restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c2315-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="c2315-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2315-108">EXAMPLES</span></span>

### <span data-ttu-id="c2315-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2315-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="c2315-110">Questo comando aggiorna un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="c2315-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="c2315-111">Il comando restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c2315-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="c2315-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2315-112">PARAMETERS</span></span>

### <span data-ttu-id="c2315-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2315-113">-DefaultProfile</span></span>
<span data-ttu-id="c2315-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2315-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2315-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2315-115">-InputObject</span></span>
<span data-ttu-id="c2315-116">Oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c2315-116">The service unit object.</span></span>

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

### <span data-ttu-id="c2315-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2315-117">-Confirm</span></span>
<span data-ttu-id="c2315-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2315-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2315-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2315-119">-WhatIf</span></span>
<span data-ttu-id="c2315-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2315-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2315-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2315-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2315-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2315-122">CommonParameters</span></span>
<span data-ttu-id="c2315-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2315-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2315-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2315-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2315-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2315-125">INPUTS</span></span>

### <span data-ttu-id="c2315-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c2315-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c2315-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2315-127">OUTPUTS</span></span>

### <span data-ttu-id="c2315-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c2315-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c2315-129">Note</span><span class="sxs-lookup"><span data-stu-id="c2315-129">NOTES</span></span>

## <span data-ttu-id="c2315-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2315-130">RELATED LINKS</span></span>
