---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519510"
---
# <span data-ttu-id="13f8d-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="13f8d-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="13f8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="13f8d-103">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="13f8d-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13f8d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13f8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f8d-105">DESCRIPTION</span></span>
<span data-ttu-id="13f8d-106">Il cmdlet **New-AzureRmServiceBusNamespace** genera nuove stringhe di connessione primarie o secondarie per lo spazio dei nomi e la regola di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="13f8d-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="13f8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13f8d-107">EXAMPLES</span></span>

### <span data-ttu-id="13f8d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13f8d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="13f8d-109">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="13f8d-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="13f8d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13f8d-110">PARAMETERS</span></span>

### <span data-ttu-id="13f8d-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="13f8d-111">-RegenerateKeys</span></span>
<span data-ttu-id="13f8d-112">Chiavi di rigenerazione: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="13f8d-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="13f8d-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13f8d-113">-ResourceGroup</span></span>
<span data-ttu-id="13f8d-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13f8d-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f8d-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13f8d-115">-Confirm</span></span>
<span data-ttu-id="13f8d-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f8d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f8d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f8d-117">-WhatIf</span></span>
<span data-ttu-id="13f8d-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13f8d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f8d-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13f8d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f8d-120">-DefaultProfile</span></span>
<span data-ttu-id="13f8d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13f8d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f8d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="13f8d-122">-Name</span></span>
<span data-ttu-id="13f8d-123">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="13f8d-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="13f8d-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13f8d-124">-Namespace</span></span>
<span data-ttu-id="13f8d-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="13f8d-125">Namespace Name.</span></span>

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

### <span data-ttu-id="13f8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f8d-126">CommonParameters</span></span>
<span data-ttu-id="13f8d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f8d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f8d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f8d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13f8d-129">INPUTS</span></span>

### <span data-ttu-id="13f8d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13f8d-130">-ResourceGroup</span></span>
 <span data-ttu-id="13f8d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="13f8d-131">System.String</span></span>
 

### <span data-ttu-id="13f8d-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="13f8d-132">-NamespaceName</span></span>
 <span data-ttu-id="13f8d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13f8d-133">System.String</span></span>
 

### <span data-ttu-id="13f8d-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="13f8d-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="13f8d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="13f8d-135">System.String</span></span>
 

### <span data-ttu-id="13f8d-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="13f8d-136">-RegenerateKeys</span></span>
 <span data-ttu-id="13f8d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="13f8d-137">System.String</span></span>

## <span data-ttu-id="13f8d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13f8d-138">OUTPUTS</span></span>

### <span data-ttu-id="13f8d-139">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="13f8d-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="13f8d-140">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-value} SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-value} PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="13f8d-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="13f8d-141">Note</span><span class="sxs-lookup"><span data-stu-id="13f8d-141">NOTES</span></span>

## <span data-ttu-id="13f8d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13f8d-142">RELATED LINKS</span></span>

