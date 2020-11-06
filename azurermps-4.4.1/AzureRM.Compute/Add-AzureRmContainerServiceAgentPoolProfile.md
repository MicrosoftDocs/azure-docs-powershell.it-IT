---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521768"
---
# <span data-ttu-id="1c397-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1c397-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="1c397-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c397-102">SYNOPSIS</span></span>
<span data-ttu-id="1c397-103">Aggiunge un profilo del pool di agente di servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="1c397-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c397-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c397-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c397-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c397-105">DESCRIPTION</span></span>
<span data-ttu-id="1c397-106">Il cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** aggiunge un profilo del pool di agenti del servizio contenitore a un oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="1c397-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="1c397-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c397-107">EXAMPLES</span></span>

### <span data-ttu-id="1c397-108">Esempio 1: aggiungere un profilo</span><span class="sxs-lookup"><span data-stu-id="1c397-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="1c397-109">Questo comando aggiunge un profilo del pool di agenti del servizio contenitore all'oggetto servizio contenitore locale.</span><span class="sxs-lookup"><span data-stu-id="1c397-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="1c397-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c397-110">PARAMETERS</span></span>

### <span data-ttu-id="1c397-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1c397-111">-ContainerService</span></span>
<span data-ttu-id="1c397-112">Specifica l'oggetto servizio contenitore a cui questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="1c397-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="1c397-113">Per ottenere un oggetto **ContainerService** , usa il cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1c397-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="1c397-114">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="1c397-114">-Count</span></span>
<span data-ttu-id="1c397-115">Specifica il numero di agenti che ospitano i contenitori.</span><span class="sxs-lookup"><span data-stu-id="1c397-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="1c397-116">I valori accettabili per questo parametro sono: numeri interi da 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="1c397-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="1c397-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="1c397-117">The default value is 1.</span></span>

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

### <span data-ttu-id="1c397-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c397-118">-DefaultProfile</span></span>
<span data-ttu-id="1c397-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c397-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c397-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="1c397-120">-DnsPrefix</span></span>
<span data-ttu-id="1c397-121">Specifica il prefisso DNS usato da questo cmdlet per creare il nome di dominio completo per il pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="1c397-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="1c397-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c397-122">-Name</span></span>
<span data-ttu-id="1c397-123">Specifica il nome del profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="1c397-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="1c397-124">Questo valore deve essere univoco nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="1c397-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="1c397-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="1c397-125">-VmSize</span></span>
<span data-ttu-id="1c397-126">Specifica le dimensioni delle macchine virtuali per gli agenti.</span><span class="sxs-lookup"><span data-stu-id="1c397-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="1c397-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c397-127">-Confirm</span></span>
<span data-ttu-id="1c397-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c397-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c397-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c397-129">-WhatIf</span></span>
<span data-ttu-id="1c397-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c397-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c397-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c397-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c397-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c397-132">CommonParameters</span></span>
<span data-ttu-id="1c397-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c397-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c397-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c397-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c397-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c397-135">INPUTS</span></span>

## <span data-ttu-id="1c397-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c397-136">OUTPUTS</span></span>

## <span data-ttu-id="1c397-137">Note</span><span class="sxs-lookup"><span data-stu-id="1c397-137">NOTES</span></span>

## <span data-ttu-id="1c397-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c397-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c397-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="1c397-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="1c397-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1c397-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
