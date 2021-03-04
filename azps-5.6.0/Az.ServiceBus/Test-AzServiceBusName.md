---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: b2bca900be878e6f89f52b1f6096e82f79ec7863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961582"
---
# <span data-ttu-id="4cf18-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="4cf18-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="4cf18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf18-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf18-103">Controlla la disponibilità del nome o alias namespace specificato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="4cf18-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="4cf18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cf18-104">SYNTAX</span></span>

### <span data-ttu-id="4cf18-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4cf18-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf18-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4cf18-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf18-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cf18-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf18-108">Il **cmdlet Test-AzServiceBusName controlla** la disponibilità del nome o alias NameSpace (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="4cf18-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4cf18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cf18-109">EXAMPLES</span></span>

### <span data-ttu-id="4cf18-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cf18-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4cf18-111">Restituisce lo stato in base alla disponibilità del nome dello spazio dei nomi 'NomeSapceName' come True</span><span class="sxs-lookup"><span data-stu-id="4cf18-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="4cf18-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4cf18-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4cf18-113">Restituisce lo stato in base alla disponibilità dello spazio dei nomi 'NomeSapceName' come Falso con motivo</span><span class="sxs-lookup"><span data-stu-id="4cf18-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="4cf18-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4cf18-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="4cf18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cf18-115">PARAMETERS</span></span>

### <span data-ttu-id="4cf18-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4cf18-116">-AliasName</span></span>
<span data-ttu-id="4cf18-117">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="4cf18-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="4cf18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf18-118">-DefaultProfile</span></span>
<span data-ttu-id="4cf18-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf18-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4cf18-120">-Namespace</span></span>
<span data-ttu-id="4cf18-121">Nome spazio dei nomi Servicebus</span><span class="sxs-lookup"><span data-stu-id="4cf18-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="4cf18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf18-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cf18-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4cf18-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4cf18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf18-124">CommonParameters</span></span>
<span data-ttu-id="4cf18-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf18-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf18-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf18-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cf18-127">INPUTS</span></span>

### <span data-ttu-id="4cf18-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf18-128">System.String</span></span>

## <span data-ttu-id="4cf18-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cf18-129">OUTPUTS</span></span>

### <span data-ttu-id="4cf18-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="4cf18-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="4cf18-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cf18-131">NOTES</span></span>

## <span data-ttu-id="4cf18-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cf18-132">RELATED LINKS</span></span>
