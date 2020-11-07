---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: a89494b155755cf716f39275debcfb7477071da2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866579"
---
# <span data-ttu-id="bd6e0-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bd6e0-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="bd6e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6e0-103">Aggiunge un profilo del pool di agente di servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd6e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd6e0-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="bd6e0-106">Il cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** aggiunge un profilo del pool di agenti del servizio contenitore a un oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="bd6e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd6e0-107">EXAMPLES</span></span>

### <span data-ttu-id="bd6e0-108">Esempio 1: aggiungere un profilo</span><span class="sxs-lookup"><span data-stu-id="bd6e0-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="bd6e0-109">Questo comando aggiunge un profilo del pool di agenti del servizio contenitore all'oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="bd6e0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd6e0-110">PARAMETERS</span></span>

### <span data-ttu-id="bd6e0-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="bd6e0-111">-ContainerService</span></span>
<span data-ttu-id="bd6e0-112">Specifica l'oggetto servizio contenitore a cui questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="bd6e0-113">Per ottenere un oggetto **ContainerService** , usa il cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="bd6e0-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-114">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="bd6e0-114">-Count</span></span>
<span data-ttu-id="bd6e0-115">Specifica il numero di agenti che ospitano i contenitori.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="bd6e0-116">I valori accettabili per questo parametro sono: numeri interi da 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="bd6e0-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6e0-118">-DefaultProfile</span></span>
<span data-ttu-id="bd6e0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="bd6e0-120">-DnsPrefix</span></span>
<span data-ttu-id="bd6e0-121">Specifica il prefisso DNS usato da questo cmdlet per creare il nome di dominio completo per il pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd6e0-122">-Name</span></span>
<span data-ttu-id="bd6e0-123">Specifica il nome del profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="bd6e0-124">Questo valore deve essere univoco nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="bd6e0-125">-VmSize</span></span>
<span data-ttu-id="bd6e0-126">Specifica le dimensioni delle macchine virtuali per gli agenti.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd6e0-127">-Confirm</span></span>
<span data-ttu-id="bd6e0-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6e0-129">-WhatIf</span></span>
<span data-ttu-id="bd6e0-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd6e0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6e0-132">CommonParameters</span></span>
<span data-ttu-id="bd6e0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6e0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd6e0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6e0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd6e0-135">INPUTS</span></span>

### <span data-ttu-id="bd6e0-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="bd6e0-136">ContainerService</span></span>
<span data-ttu-id="bd6e0-137">Il parametro ' ContainerService ' accetta il valore di tipo ' ContainerService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bd6e0-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="bd6e0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd6e0-138">OUTPUTS</span></span>

### <span data-ttu-id="bd6e0-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="bd6e0-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="bd6e0-140">Note</span><span class="sxs-lookup"><span data-stu-id="bd6e0-140">NOTES</span></span>

## <span data-ttu-id="bd6e0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd6e0-141">RELATED LINKS</span></span>

[<span data-ttu-id="bd6e0-142">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="bd6e0-142">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="bd6e0-143">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="bd6e0-143">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
