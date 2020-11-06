---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518203"
---
# <span data-ttu-id="93d64-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="93d64-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="93d64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93d64-102">SYNOPSIS</span></span>
<span data-ttu-id="93d64-103">Aggiunge un profilo del pool di agente di servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="93d64-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93d64-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d64-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93d64-105">DESCRIPTION</span></span>
<span data-ttu-id="93d64-106">Il cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** aggiunge un profilo del pool di agenti del servizio contenitore a un oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="93d64-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="93d64-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93d64-107">EXAMPLES</span></span>

### <span data-ttu-id="93d64-108">Esempio 1: aggiungere un profilo</span><span class="sxs-lookup"><span data-stu-id="93d64-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="93d64-109">Questo comando aggiunge un profilo del pool di agenti del servizio contenitore all'oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="93d64-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="93d64-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93d64-110">PARAMETERS</span></span>

### <span data-ttu-id="93d64-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="93d64-111">-ContainerService</span></span>
<span data-ttu-id="93d64-112">Specifica l'oggetto servizio contenitore a cui questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="93d64-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="93d64-113">Per ottenere un oggetto **ContainerService** , usa il cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="93d64-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d64-114">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="93d64-114">-Count</span></span>
<span data-ttu-id="93d64-115">Specifica il numero di agenti che ospitano i contenitori.</span><span class="sxs-lookup"><span data-stu-id="93d64-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="93d64-116">I valori accettabili per questo parametro sono: numeri interi da 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="93d64-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="93d64-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="93d64-117">The default value is 1.</span></span>

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

### <span data-ttu-id="93d64-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="93d64-118">-DnsPrefix</span></span>
<span data-ttu-id="93d64-119">Specifica il prefisso DNS usato da questo cmdlet per creare il nome di dominio completo per il pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="93d64-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="93d64-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="93d64-120">-Name</span></span>
<span data-ttu-id="93d64-121">Specifica il nome del profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="93d64-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="93d64-122">Questo valore deve essere univoco nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="93d64-122">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="93d64-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="93d64-123">-VmSize</span></span>
<span data-ttu-id="93d64-124">Specifica le dimensioni delle macchine virtuali per gli agenti.</span><span class="sxs-lookup"><span data-stu-id="93d64-124">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="93d64-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93d64-125">-Confirm</span></span>
<span data-ttu-id="93d64-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93d64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d64-127">-WhatIf</span></span>
<span data-ttu-id="93d64-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d64-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93d64-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d64-130">CommonParameters</span></span>
<span data-ttu-id="93d64-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d64-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d64-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d64-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93d64-133">INPUTS</span></span>

### <span data-ttu-id="93d64-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="93d64-134">None</span></span>
<span data-ttu-id="93d64-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="93d64-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93d64-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93d64-136">OUTPUTS</span></span>

## <span data-ttu-id="93d64-137">Note</span><span class="sxs-lookup"><span data-stu-id="93d64-137">NOTES</span></span>

## <span data-ttu-id="93d64-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93d64-138">RELATED LINKS</span></span>

[<span data-ttu-id="93d64-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="93d64-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="93d64-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="93d64-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
