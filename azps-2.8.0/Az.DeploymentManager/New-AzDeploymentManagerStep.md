---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674612"
---
# <span data-ttu-id="9c629-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="9c629-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="9c629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c629-102">SYNOPSIS</span></span>
<span data-ttu-id="9c629-103">Crea un passaggio.</span><span class="sxs-lookup"><span data-stu-id="9c629-103">Creates a step.</span></span>

## <span data-ttu-id="9c629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c629-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c629-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c629-105">DESCRIPTION</span></span>
<span data-ttu-id="9c629-106">Il cmdlet **New-AzDeploymentManagerStep** crea un passaggio di distribuzione a cui è possibile fare riferimento in rollout.</span><span class="sxs-lookup"><span data-stu-id="9c629-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="9c629-107">Specificare il *nome* , *ResourceGroupName* e le proprietà obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="9c629-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="9c629-108">Puoi modificare l'oggetto restituito localmente e quindi applicare le modifiche apportate al passaggio usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="9c629-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="9c629-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c629-109">EXAMPLES</span></span>

### <span data-ttu-id="9c629-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c629-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="9c629-111">Crea un passaggio in ContosoResourceGroup con il nome ContosoService1WaitStep con il centro degli Stati Uniti come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c629-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="9c629-112">La proprietà Duration fornisce la durata in cui l'implementazione verrà attesa prima di eseguire il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="9c629-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="9c629-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c629-113">PARAMETERS</span></span>

### <span data-ttu-id="9c629-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c629-114">-DefaultProfile</span></span>
<span data-ttu-id="9c629-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c629-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c629-116">-Durata</span><span class="sxs-lookup"><span data-stu-id="9c629-116">-Duration</span></span>
<span data-ttu-id="9c629-117">Durata da attendere in formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="9c629-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="9c629-118">Ad esempio: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="9c629-118">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c629-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9c629-119">-Location</span></span>
<span data-ttu-id="9c629-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c629-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c629-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c629-121">-Name</span></span>
<span data-ttu-id="9c629-122">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="9c629-122">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c629-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c629-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c629-124">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9c629-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c629-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c629-125">-Tag</span></span>
<span data-ttu-id="9c629-126">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9c629-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c629-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c629-127">-Confirm</span></span>
<span data-ttu-id="9c629-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c629-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c629-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c629-129">-WhatIf</span></span>
<span data-ttu-id="9c629-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c629-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c629-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c629-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c629-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c629-132">CommonParameters</span></span>
<span data-ttu-id="9c629-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c629-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c629-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c629-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c629-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c629-135">INPUTS</span></span>

### <span data-ttu-id="9c629-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c629-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c629-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c629-137">OUTPUTS</span></span>

### <span data-ttu-id="9c629-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="9c629-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="9c629-139">Note</span><span class="sxs-lookup"><span data-stu-id="9c629-139">NOTES</span></span>

## <span data-ttu-id="9c629-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c629-140">RELATED LINKS</span></span>
