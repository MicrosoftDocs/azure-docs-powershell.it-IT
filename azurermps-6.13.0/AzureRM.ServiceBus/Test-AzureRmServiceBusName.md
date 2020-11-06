---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513412"
---
# <span data-ttu-id="98c19-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="98c19-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="98c19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98c19-102">SYNOPSIS</span></span>
<span data-ttu-id="98c19-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="98c19-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98c19-104">SYNTAX</span></span>

### <span data-ttu-id="98c19-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="98c19-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c19-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="98c19-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98c19-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c19-107">DESCRIPTION</span></span>
<span data-ttu-id="98c19-108">Il cmdlet **test-AzureRmServiceBusName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="98c19-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="98c19-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98c19-109">EXAMPLES</span></span>

### <span data-ttu-id="98c19-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98c19-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="98c19-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero</span><span class="sxs-lookup"><span data-stu-id="98c19-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="98c19-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="98c19-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="98c19-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="98c19-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="98c19-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="98c19-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="98c19-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98c19-115">PARAMETERS</span></span>

### <span data-ttu-id="98c19-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="98c19-116">-AliasName</span></span>
<span data-ttu-id="98c19-117">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="98c19-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c19-118">-DefaultProfile</span></span>
<span data-ttu-id="98c19-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98c19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c19-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="98c19-120">-Namespace</span></span>
<span data-ttu-id="98c19-121">Nome dello spazio dei nomi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98c19-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c19-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c19-122">-ResourceGroupName</span></span>
<span data-ttu-id="98c19-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="98c19-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c19-124">CommonParameters</span></span>
<span data-ttu-id="98c19-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c19-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c19-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c19-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98c19-127">INPUTS</span></span>

### <span data-ttu-id="98c19-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98c19-128">System.String</span></span>

## <span data-ttu-id="98c19-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98c19-129">OUTPUTS</span></span>

### <span data-ttu-id="98c19-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="98c19-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="98c19-131">Note</span><span class="sxs-lookup"><span data-stu-id="98c19-131">NOTES</span></span>

## <span data-ttu-id="98c19-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98c19-132">RELATED LINKS</span></span>
