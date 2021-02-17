---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: e6f2495392eed73e5576d8502f86a08e325337f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183614"
---
# <span data-ttu-id="9c860-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="9c860-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="9c860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c860-102">SYNOPSIS</span></span>
<span data-ttu-id="9c860-103">Recupera la coppia di chiavi di amministrazione del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9c860-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c860-104">SYNTAX</span></span>

### <span data-ttu-id="9c860-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c860-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c860-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c860-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c860-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c860-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c860-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c860-108">DESCRIPTION</span></span>
<span data-ttu-id="9c860-109">Il cmdlet **Get-AzSearchAdminKeyPair** ottiene la coppia di chiavi di amministrazione del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9c860-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c860-110">EXAMPLES</span></span>

### <span data-ttu-id="9c860-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c860-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="9c860-112">L'esempio ottiene la coppia di chiavi di amministratore del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9c860-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c860-113">PARAMETERS</span></span>

### <span data-ttu-id="9c860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c860-114">-DefaultProfile</span></span>
<span data-ttu-id="9c860-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c860-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c860-116">-ParentObject</span></span>
<span data-ttu-id="9c860-117">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c860-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9c860-118">-ParentResourceId</span></span>
<span data-ttu-id="9c860-119">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-119">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c860-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c860-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c860-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c860-121">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c860-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9c860-122">-ServiceName</span></span>
<span data-ttu-id="9c860-123">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c860-123">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c860-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c860-124">CommonParameters</span></span>
<span data-ttu-id="9c860-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c860-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c860-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c860-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c860-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c860-127">INPUTS</span></span>

### <span data-ttu-id="9c860-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9c860-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="9c860-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9c860-129">System.String</span></span>

## <span data-ttu-id="9c860-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c860-130">OUTPUTS</span></span>

### <span data-ttu-id="9c860-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="9c860-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="9c860-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c860-132">NOTES</span></span>

## <span data-ttu-id="9c860-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c860-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c860-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="9c860-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
