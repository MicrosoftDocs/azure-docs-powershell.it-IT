---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521144"
---
# <span data-ttu-id="620b7-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="620b7-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="620b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="620b7-102">SYNOPSIS</span></span>
<span data-ttu-id="620b7-103">Abilita la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="620b7-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="620b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="620b7-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="620b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="620b7-105">DESCRIPTION</span></span>
<span data-ttu-id="620b7-106">Il cmdlet **set-AzureRmRedisCacheDiagnostics** Abilita la diagnostica per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="620b7-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="620b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="620b7-107">EXAMPLES</span></span>

### <span data-ttu-id="620b7-108">Esempio 1: abilitare la diagnostica</span><span class="sxs-lookup"><span data-stu-id="620b7-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="620b7-109">Questo comando consente di abilitare la diagnostica per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="620b7-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="620b7-110">Questo comando consente di abilitare la diagnostica o aggiornare l'account di archiviazione per tutte le cache di Azure Redis nella stessa area geografica per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="620b7-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="620b7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="620b7-111">PARAMETERS</span></span>

### <span data-ttu-id="620b7-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="620b7-112">-Name</span></span>
<span data-ttu-id="620b7-113">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="620b7-113">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620b7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="620b7-114">-ResourceGroupName</span></span>
<span data-ttu-id="620b7-115">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="620b7-115">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620b7-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="620b7-116">-StorageAccountId</span></span>
<span data-ttu-id="620b7-117">Specifica l'ID risorsa dell'account di archiviazione usato per archiviare i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="620b7-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620b7-118">-DefaultProfile</span></span>
<span data-ttu-id="620b7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="620b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="620b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620b7-120">CommonParameters</span></span>
<span data-ttu-id="620b7-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620b7-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620b7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620b7-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="620b7-123">INPUTS</span></span>

### <span data-ttu-id="620b7-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="620b7-124">None</span></span>

## <span data-ttu-id="620b7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="620b7-125">OUTPUTS</span></span>

### <span data-ttu-id="620b7-126">Void</span><span class="sxs-lookup"><span data-stu-id="620b7-126">Void</span></span>

## <span data-ttu-id="620b7-127">Note</span><span class="sxs-lookup"><span data-stu-id="620b7-127">NOTES</span></span>
* <span data-ttu-id="620b7-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="620b7-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="620b7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="620b7-129">RELATED LINKS</span></span>

[<span data-ttu-id="620b7-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="620b7-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


