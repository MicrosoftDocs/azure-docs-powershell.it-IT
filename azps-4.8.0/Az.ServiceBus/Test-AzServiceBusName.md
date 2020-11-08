---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031053"
---
# <span data-ttu-id="07079-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="07079-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="07079-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07079-102">SYNOPSIS</span></span>
<span data-ttu-id="07079-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="07079-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="07079-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07079-104">SYNTAX</span></span>

### <span data-ttu-id="07079-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07079-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07079-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07079-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07079-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07079-107">DESCRIPTION</span></span>
<span data-ttu-id="07079-108">Il cmdlet **test-AzServiceBusName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="07079-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="07079-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07079-109">EXAMPLES</span></span>

### <span data-ttu-id="07079-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07079-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="07079-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero</span><span class="sxs-lookup"><span data-stu-id="07079-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="07079-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="07079-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="07079-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="07079-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="07079-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="07079-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="07079-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07079-115">PARAMETERS</span></span>

### <span data-ttu-id="07079-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="07079-116">-AliasName</span></span>
<span data-ttu-id="07079-117">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="07079-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="07079-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07079-118">-DefaultProfile</span></span>
<span data-ttu-id="07079-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07079-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07079-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07079-120">-Namespace</span></span>
<span data-ttu-id="07079-121">Nome dello spazio dei nomi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07079-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="07079-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07079-122">-ResourceGroupName</span></span>
<span data-ttu-id="07079-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="07079-123">Resource Group Name</span></span>

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

### <span data-ttu-id="07079-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07079-124">CommonParameters</span></span>
<span data-ttu-id="07079-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07079-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07079-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07079-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07079-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07079-127">INPUTS</span></span>

### <span data-ttu-id="07079-128">System. String</span><span class="sxs-lookup"><span data-stu-id="07079-128">System.String</span></span>

## <span data-ttu-id="07079-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07079-129">OUTPUTS</span></span>

### <span data-ttu-id="07079-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="07079-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="07079-131">Note</span><span class="sxs-lookup"><span data-stu-id="07079-131">NOTES</span></span>

## <span data-ttu-id="07079-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07079-132">RELATED LINKS</span></span>
