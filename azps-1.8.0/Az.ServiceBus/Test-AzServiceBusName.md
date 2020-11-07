---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677088"
---
# <span data-ttu-id="42d67-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="42d67-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="42d67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42d67-102">SYNOPSIS</span></span>
<span data-ttu-id="42d67-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="42d67-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="42d67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42d67-104">SYNTAX</span></span>

### <span data-ttu-id="42d67-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42d67-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d67-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42d67-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d67-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42d67-107">DESCRIPTION</span></span>
<span data-ttu-id="42d67-108">Il cmdlet **test-AzServiceBusName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="42d67-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="42d67-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42d67-109">EXAMPLES</span></span>

### <span data-ttu-id="42d67-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42d67-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="42d67-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero</span><span class="sxs-lookup"><span data-stu-id="42d67-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="42d67-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="42d67-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="42d67-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="42d67-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="42d67-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="42d67-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="42d67-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42d67-115">PARAMETERS</span></span>

### <span data-ttu-id="42d67-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="42d67-116">-AliasName</span></span>
<span data-ttu-id="42d67-117">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="42d67-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="42d67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d67-118">-DefaultProfile</span></span>
<span data-ttu-id="42d67-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42d67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d67-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42d67-120">-Namespace</span></span>
<span data-ttu-id="42d67-121">Nome dello spazio dei nomi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42d67-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="42d67-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d67-122">-ResourceGroupName</span></span>
<span data-ttu-id="42d67-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="42d67-123">Resource Group Name</span></span>

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

### <span data-ttu-id="42d67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d67-124">CommonParameters</span></span>
<span data-ttu-id="42d67-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d67-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d67-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d67-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42d67-127">INPUTS</span></span>

### <span data-ttu-id="42d67-128">System. String</span><span class="sxs-lookup"><span data-stu-id="42d67-128">System.String</span></span>

## <span data-ttu-id="42d67-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42d67-129">OUTPUTS</span></span>

### <span data-ttu-id="42d67-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="42d67-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="42d67-131">Note</span><span class="sxs-lookup"><span data-stu-id="42d67-131">NOTES</span></span>

## <span data-ttu-id="42d67-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42d67-132">RELATED LINKS</span></span>