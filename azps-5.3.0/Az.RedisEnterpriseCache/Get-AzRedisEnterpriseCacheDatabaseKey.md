---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474347"
---
# <span data-ttu-id="395de-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="395de-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="395de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="395de-102">SYNOPSIS</span></span>
<span data-ttu-id="395de-103">Recupera i tasti di scelta per il database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="395de-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="395de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="395de-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="395de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="395de-105">DESCRIPTION</span></span>
<span data-ttu-id="395de-106">Recupera i tasti di scelta per il database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="395de-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="395de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="395de-107">EXAMPLES</span></span>

### <span data-ttu-id="395de-108">Esempio 1: ottenere i tasti di scelta del database</span><span class="sxs-lookup"><span data-stu-id="395de-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="395de-109">Questo comando consente di ottenere le chiavi di accesso segrete usate per l'autenticazione delle connessioni al database della cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="395de-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="395de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="395de-110">PARAMETERS</span></span>

### <span data-ttu-id="395de-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="395de-111">-ClusterName</span></span>
<span data-ttu-id="395de-112">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="395de-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395de-113">-DefaultProfile</span></span>
<span data-ttu-id="395de-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="395de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395de-115">-ResourceGroupName</span></span>
<span data-ttu-id="395de-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="395de-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395de-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="395de-117">-SubscriptionId</span></span>
<span data-ttu-id="395de-118">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="395de-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="395de-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="395de-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395de-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="395de-120">-Confirm</span></span>
<span data-ttu-id="395de-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="395de-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395de-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395de-122">-WhatIf</span></span>
<span data-ttu-id="395de-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="395de-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395de-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="395de-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395de-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395de-125">CommonParameters</span></span>
<span data-ttu-id="395de-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395de-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395de-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="395de-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395de-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="395de-128">INPUTS</span></span>

## <span data-ttu-id="395de-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="395de-129">OUTPUTS</span></span>

### <span data-ttu-id="395de-130">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="395de-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="395de-131">Note</span><span class="sxs-lookup"><span data-stu-id="395de-131">NOTES</span></span>

<span data-ttu-id="395de-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="395de-132">ALIASES</span></span>

## <span data-ttu-id="395de-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="395de-133">RELATED LINKS</span></span>

