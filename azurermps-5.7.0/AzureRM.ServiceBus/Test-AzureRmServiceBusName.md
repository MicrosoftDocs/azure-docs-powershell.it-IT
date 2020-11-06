---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512271"
---
# <span data-ttu-id="61aea-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="61aea-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="61aea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61aea-102">SYNOPSIS</span></span>
<span data-ttu-id="61aea-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="61aea-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61aea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61aea-104">SYNTAX</span></span>

### <span data-ttu-id="61aea-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="61aea-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61aea-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="61aea-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61aea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61aea-107">DESCRIPTION</span></span>
<span data-ttu-id="61aea-108">Il cmdlet **test-AzureRmServiceBusName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="61aea-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="61aea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61aea-109">EXAMPLES</span></span>

### <span data-ttu-id="61aea-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61aea-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="61aea-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero</span><span class="sxs-lookup"><span data-stu-id="61aea-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="61aea-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="61aea-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="61aea-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="61aea-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="61aea-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="61aea-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="61aea-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61aea-115">PARAMETERS</span></span>

### <span data-ttu-id="61aea-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="61aea-116">-AliasName</span></span>
<span data-ttu-id="61aea-117">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="61aea-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aea-118">-DefaultProfile</span></span>
<span data-ttu-id="61aea-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61aea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61aea-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="61aea-120">-Namespace</span></span>
<span data-ttu-id="61aea-121">Nome dello spazio dei nomi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="61aea-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61aea-122">-ResourceGroupName</span></span>
<span data-ttu-id="61aea-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="61aea-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aea-124">CommonParameters</span></span>
<span data-ttu-id="61aea-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="61aea-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61aea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aea-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61aea-127">INPUTS</span></span>

### <span data-ttu-id="61aea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61aea-128">System.String</span></span>


## <span data-ttu-id="61aea-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61aea-129">OUTPUTS</span></span>

### <span data-ttu-id="61aea-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="61aea-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="61aea-131">Note</span><span class="sxs-lookup"><span data-stu-id="61aea-131">NOTES</span></span>

## <span data-ttu-id="61aea-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61aea-132">RELATED LINKS</span></span>
