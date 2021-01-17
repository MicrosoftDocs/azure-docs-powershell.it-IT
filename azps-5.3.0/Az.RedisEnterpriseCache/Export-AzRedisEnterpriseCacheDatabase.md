---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474353"
---
# <span data-ttu-id="ae8fd-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ae8fd-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ae8fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8fd-103">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="ae8fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae8fd-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ae8fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae8fd-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8fd-106">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="ae8fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae8fd-107">EXAMPLES</span></span>

### <span data-ttu-id="ae8fd-108">Esempio 1: esportare il database</span><span class="sxs-lookup"><span data-stu-id="ae8fd-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ae8fd-109">Questo comando Esporta il database della cache di redis Enterprise denominata cache in un file di database.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="ae8fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae8fd-110">PARAMETERS</span></span>

### <span data-ttu-id="ae8fd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae8fd-111">-AsJob</span></span>
<span data-ttu-id="ae8fd-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ae8fd-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8fd-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ae8fd-113">-ClusterName</span></span>
<span data-ttu-id="ae8fd-114">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ae8fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8fd-115">-DefaultProfile</span></span>
<span data-ttu-id="ae8fd-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae8fd-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ae8fd-117">-NoWait</span></span>
<span data-ttu-id="ae8fd-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ae8fd-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8fd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae8fd-119">-PassThru</span></span>
<span data-ttu-id="ae8fd-120">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ae8fd-120">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae8fd-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae8fd-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="ae8fd-123">-SasUri</span></span>
<span data-ttu-id="ae8fd-124">URI SAS per la directory di destinazione da esportare in</span><span class="sxs-lookup"><span data-stu-id="ae8fd-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="ae8fd-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae8fd-125">-SubscriptionId</span></span>
<span data-ttu-id="ae8fd-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae8fd-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8fd-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae8fd-128">-Confirm</span></span>
<span data-ttu-id="ae8fd-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae8fd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8fd-130">-WhatIf</span></span>
<span data-ttu-id="ae8fd-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae8fd-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae8fd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8fd-133">CommonParameters</span></span>
<span data-ttu-id="ae8fd-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae8fd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8fd-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae8fd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8fd-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae8fd-136">INPUTS</span></span>

## <span data-ttu-id="ae8fd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae8fd-137">OUTPUTS</span></span>

### <span data-ttu-id="ae8fd-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae8fd-138">System.Boolean</span></span>

## <span data-ttu-id="ae8fd-139">Note</span><span class="sxs-lookup"><span data-stu-id="ae8fd-139">NOTES</span></span>

<span data-ttu-id="ae8fd-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ae8fd-140">ALIASES</span></span>

## <span data-ttu-id="ae8fd-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae8fd-141">RELATED LINKS</span></span>

