---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 4a356af4090fefe25956fb421b0df409e1edd79b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684847"
---
# <span data-ttu-id="72ca7-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="72ca7-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="72ca7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="72ca7-103">Aggiunge un profilo del pool di agente di servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="72ca7-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="72ca7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72ca7-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ca7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72ca7-105">DESCRIPTION</span></span>
<span data-ttu-id="72ca7-106">Il cmdlet **Add-AzContainerServiceAgentPoolProfile** aggiunge un profilo del pool di agenti del servizio contenitore a un oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="72ca7-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="72ca7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72ca7-107">EXAMPLES</span></span>

### <span data-ttu-id="72ca7-108">Esempio 1: aggiungere un profilo</span><span class="sxs-lookup"><span data-stu-id="72ca7-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="72ca7-109">Questo comando aggiunge un profilo del pool di agenti del servizio contenitore all'oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="72ca7-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="72ca7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="72ca7-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="72ca7-111">-ContainerService</span></span>
<span data-ttu-id="72ca7-112">Specifica l'oggetto servizio contenitore a cui questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="72ca7-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="72ca7-113">Per ottenere un oggetto **ContainerService** , usa il cmdlet [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="72ca7-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca7-114">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="72ca7-114">-Count</span></span>
<span data-ttu-id="72ca7-115">Specifica il numero di agenti che ospitano i contenitori.</span><span class="sxs-lookup"><span data-stu-id="72ca7-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="72ca7-116">I valori accettabili per questo parametro sono: numeri interi da 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="72ca7-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="72ca7-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="72ca7-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ca7-118">-DefaultProfile</span></span>
<span data-ttu-id="72ca7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72ca7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72ca7-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="72ca7-120">-DnsPrefix</span></span>
<span data-ttu-id="72ca7-121">Specifica il prefisso DNS usato da questo cmdlet per creare il nome di dominio completo per il pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="72ca7-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="72ca7-122">-Name</span></span>
<span data-ttu-id="72ca7-123">Specifica il nome del profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="72ca7-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="72ca7-124">Questo valore deve essere univoco nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="72ca7-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca7-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="72ca7-125">-VmSize</span></span>
<span data-ttu-id="72ca7-126">Specifica le dimensioni delle macchine virtuali per gli agenti.</span><span class="sxs-lookup"><span data-stu-id="72ca7-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca7-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72ca7-127">-Confirm</span></span>
<span data-ttu-id="72ca7-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ca7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ca7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ca7-129">-WhatIf</span></span>
<span data-ttu-id="72ca7-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72ca7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72ca7-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72ca7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ca7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ca7-132">CommonParameters</span></span>
<span data-ttu-id="72ca7-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ca7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ca7-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ca7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ca7-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72ca7-135">INPUTS</span></span>

### <span data-ttu-id="72ca7-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="72ca7-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="72ca7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72ca7-137">System.String</span></span>

### <span data-ttu-id="72ca7-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="72ca7-138">System.Int32</span></span>

## <span data-ttu-id="72ca7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72ca7-139">OUTPUTS</span></span>

### <span data-ttu-id="72ca7-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="72ca7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="72ca7-141">Note</span><span class="sxs-lookup"><span data-stu-id="72ca7-141">NOTES</span></span>

## <span data-ttu-id="72ca7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72ca7-142">RELATED LINKS</span></span>

[<span data-ttu-id="72ca7-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="72ca7-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="72ca7-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="72ca7-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
