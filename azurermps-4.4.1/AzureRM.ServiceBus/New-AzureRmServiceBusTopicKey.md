---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512972"
---
# <span data-ttu-id="f0543-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="f0543-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="f0543-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0543-102">SYNOPSIS</span></span>
<span data-ttu-id="f0543-103">Rigenera le stringhe di connessione primarie o secondarie per l'argomento Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f0543-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0543-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0543-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0543-105">DESCRIPTION</span></span>
<span data-ttu-id="f0543-106">Il cmdlet **New-AzureRmServiceBusTopicKey** genera una nuova stringa di connessione primaria o secondaria per l'argomento e la regola di autorizzazione di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="f0543-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="f0543-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0543-107">EXAMPLES</span></span>

### <span data-ttu-id="f0543-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0543-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="f0543-109">Rigenera la stringa di connessione primaria per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f0543-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="f0543-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f0543-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="f0543-111">Rigenera la stringa di connessione secondaria per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f0543-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="f0543-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0543-112">PARAMETERS</span></span>

### <span data-ttu-id="f0543-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f0543-113">-RegenerateKeys</span></span>
<span data-ttu-id="f0543-114">Specifica se rigenerare le chiavi primarie o secondarie.</span><span class="sxs-lookup"><span data-stu-id="f0543-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0543-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0543-115">-ResourceGroup</span></span>
<span data-ttu-id="f0543-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0543-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0543-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0543-117">-Confirm</span></span>
<span data-ttu-id="f0543-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0543-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0543-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0543-119">-WhatIf</span></span>
<span data-ttu-id="f0543-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0543-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0543-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0543-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0543-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0543-122">-DefaultProfile</span></span>
<span data-ttu-id="f0543-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0543-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0543-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0543-124">-Name</span></span>
<span data-ttu-id="f0543-125">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0543-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0543-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0543-126">-Namespace</span></span>
<span data-ttu-id="f0543-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f0543-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0543-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="f0543-128">-Topic</span></span>
<span data-ttu-id="f0543-129">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="f0543-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0543-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0543-130">CommonParameters</span></span>
<span data-ttu-id="f0543-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0543-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0543-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0543-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0543-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0543-133">INPUTS</span></span>

### <span data-ttu-id="f0543-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0543-134">-ResourceGroup</span></span>
 <span data-ttu-id="f0543-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f0543-135">System.String</span></span>
 

### <span data-ttu-id="f0543-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f0543-136">-NamespaceName</span></span>
 <span data-ttu-id="f0543-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f0543-137">System.String</span></span>
 

### <span data-ttu-id="f0543-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f0543-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f0543-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f0543-139">System.String</span></span>
 

### <span data-ttu-id="f0543-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="f0543-140">-TopicName</span></span>
 <span data-ttu-id="f0543-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f0543-141">System.String</span></span>
 

### <span data-ttu-id="f0543-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f0543-142">-RegenerateKeys</span></span>
 <span data-ttu-id="f0543-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f0543-143">System.String</span></span>

## <span data-ttu-id="f0543-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0543-144">OUTPUTS</span></span>

### <span data-ttu-id="f0543-145">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f0543-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="f0543-146">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-topi c_exampl1 SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-topi c_exampl1 PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f0543-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="f0543-147">Note</span><span class="sxs-lookup"><span data-stu-id="f0543-147">NOTES</span></span>

## <span data-ttu-id="f0543-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0543-148">RELATED LINKS</span></span>

