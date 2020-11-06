---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516011"
---
# <span data-ttu-id="93ff5-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="93ff5-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="93ff5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="93ff5-103">Ottiene le stringhe di connessione primarie e secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="93ff5-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ff5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93ff5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ff5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="93ff5-106">Il cmdlet **Get-AzureRmServiceBusNamespaceKey** restituisce le stringhe di connessione primarie e secondarie per lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="93ff5-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="93ff5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93ff5-107">EXAMPLES</span></span>

### <span data-ttu-id="93ff5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93ff5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="93ff5-109">Stringa di connessione primaria e secondaria allo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="93ff5-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="93ff5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93ff5-110">PARAMETERS</span></span>

### <span data-ttu-id="93ff5-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93ff5-111">-ResourceGroup</span></span>
<span data-ttu-id="93ff5-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93ff5-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="93ff5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ff5-113">-DefaultProfile</span></span>
<span data-ttu-id="93ff5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93ff5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ff5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="93ff5-115">-Name</span></span>
<span data-ttu-id="93ff5-116">Nome AuthorizationRule dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="93ff5-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="93ff5-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93ff5-117">-Namespace</span></span>
<span data-ttu-id="93ff5-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="93ff5-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="93ff5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ff5-119">CommonParameters</span></span>
<span data-ttu-id="93ff5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ff5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ff5-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ff5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ff5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93ff5-122">INPUTS</span></span>

### <span data-ttu-id="93ff5-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93ff5-123">-ResourceGroup</span></span>
 <span data-ttu-id="93ff5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="93ff5-124">System.String</span></span>
 

### <span data-ttu-id="93ff5-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="93ff5-125">-NamespaceName</span></span>
 <span data-ttu-id="93ff5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="93ff5-126">System.String</span></span>
 

### <span data-ttu-id="93ff5-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="93ff5-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="93ff5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="93ff5-128">System.String</span></span>

## <span data-ttu-id="93ff5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93ff5-129">OUTPUTS</span></span>

### <span data-ttu-id="93ff5-130">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="93ff5-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="93ff5-131">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="93ff5-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="93ff5-132">Note</span><span class="sxs-lookup"><span data-stu-id="93ff5-132">NOTES</span></span>

## <span data-ttu-id="93ff5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93ff5-133">RELATED LINKS</span></span>

