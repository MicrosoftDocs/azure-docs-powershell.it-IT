---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490853"
---
# <span data-ttu-id="28a4d-101">New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="28a4d-101">New-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="28a4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="28a4d-103">Crea un nuovo passaggio di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="28a4d-103">Creates a new deployment step.</span></span>

## <span data-ttu-id="28a4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28a4d-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28a4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="28a4d-106">Il cmdlet **New-AzureRmDeploymentManagerStep** crea un passaggio di distribuzione a cui è possibile fare riferimento in rollout.</span><span class="sxs-lookup"><span data-stu-id="28a4d-106">The **New-AzureRmDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="28a4d-107">Specificare il *nome* , *ResourceGroupName* e le proprietà obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="28a4d-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="28a4d-108">Puoi modificare l'oggetto restituito localmente e quindi applicare le modifiche apportate al passaggio usando il cmdlet Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="28a4d-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="28a4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28a4d-109">EXAMPLES</span></span>

### <span data-ttu-id="28a4d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28a4d-110">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="28a4d-111">Crea un passaggio in ContosoResourceGroup con il nome ContosoService1WaitStep con il centro degli Stati Uniti come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28a4d-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="28a4d-112">La proprietà Duration fornisce la durata in cui l'implementazione verrà attesa prima di eseguire il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="28a4d-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="28a4d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28a4d-113">PARAMETERS</span></span>

### <span data-ttu-id="28a4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a4d-114">-DefaultProfile</span></span>
<span data-ttu-id="28a4d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28a4d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a4d-116">-Durata</span><span class="sxs-lookup"><span data-stu-id="28a4d-116">-Duration</span></span>
<span data-ttu-id="28a4d-117">Durata da attendere in formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="28a4d-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="28a4d-118">Ad esempio: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="28a4d-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="28a4d-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="28a4d-119">-Location</span></span>
<span data-ttu-id="28a4d-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28a4d-120">The location of the resource.</span></span>

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

### <span data-ttu-id="28a4d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="28a4d-121">-Name</span></span>
<span data-ttu-id="28a4d-122">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="28a4d-122">The name of the step.</span></span>

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

### <span data-ttu-id="28a4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="28a4d-124">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="28a4d-124">The resource group.</span></span>

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

### <span data-ttu-id="28a4d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="28a4d-125">-Tag</span></span>
<span data-ttu-id="28a4d-126">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="28a4d-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28a4d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28a4d-127">-Confirm</span></span>
<span data-ttu-id="28a4d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28a4d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a4d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a4d-129">-WhatIf</span></span>
<span data-ttu-id="28a4d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28a4d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28a4d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28a4d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a4d-132">CommonParameters</span></span>
<span data-ttu-id="28a4d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="28a4d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a4d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a4d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28a4d-135">INPUTS</span></span>

### <span data-ttu-id="28a4d-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="28a4d-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="28a4d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28a4d-137">OUTPUTS</span></span>

### <span data-ttu-id="28a4d-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="28a4d-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="28a4d-139">Note</span><span class="sxs-lookup"><span data-stu-id="28a4d-139">NOTES</span></span>

## <span data-ttu-id="28a4d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28a4d-140">RELATED LINKS</span></span>
