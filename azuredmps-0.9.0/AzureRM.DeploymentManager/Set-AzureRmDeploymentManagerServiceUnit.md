---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491278"
---
# <span data-ttu-id="cd535-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cd535-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="cd535-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd535-102">SYNOPSIS</span></span>
<span data-ttu-id="cd535-103">Aggiorna un'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="cd535-103">Updates a service unit.</span></span>

## <span data-ttu-id="cd535-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd535-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd535-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd535-105">DESCRIPTION</span></span>
<span data-ttu-id="cd535-106">Il cmdlet **set-AzureRmDeploymentManagerServiceUnit** aggiorna un'unità di servizio con l'oggetto unità di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="cd535-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="cd535-107">Il cmdlet restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cd535-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="cd535-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd535-108">EXAMPLES</span></span>

### <span data-ttu-id="cd535-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd535-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="cd535-110">Questo comando aggiorna un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="cd535-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="cd535-111">Il comando restituisce l'oggetto unità di servizio aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cd535-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="cd535-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd535-112">PARAMETERS</span></span>

### <span data-ttu-id="cd535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd535-113">-DefaultProfile</span></span>
<span data-ttu-id="cd535-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd535-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd535-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cd535-115">-ServiceUnit</span></span>
<span data-ttu-id="cd535-116">Oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="cd535-116">The service unit object.</span></span>

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

### <span data-ttu-id="cd535-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd535-117">-Confirm</span></span>
<span data-ttu-id="cd535-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd535-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd535-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd535-119">-WhatIf</span></span>
<span data-ttu-id="cd535-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd535-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd535-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd535-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd535-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd535-122">CommonParameters</span></span>
<span data-ttu-id="cd535-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd535-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd535-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd535-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd535-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd535-125">INPUTS</span></span>

### <span data-ttu-id="cd535-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cd535-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cd535-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd535-127">OUTPUTS</span></span>

### <span data-ttu-id="cd535-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cd535-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cd535-129">Note</span><span class="sxs-lookup"><span data-stu-id="cd535-129">NOTES</span></span>

## <span data-ttu-id="cd535-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd535-130">RELATED LINKS</span></span>

[<span data-ttu-id="cd535-131">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cd535-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="cd535-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cd535-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="cd535-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cd535-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)