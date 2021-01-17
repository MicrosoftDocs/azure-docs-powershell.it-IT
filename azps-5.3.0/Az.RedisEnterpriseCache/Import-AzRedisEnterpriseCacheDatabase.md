---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378234"
---
# <span data-ttu-id="ad41e-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ad41e-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ad41e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad41e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad41e-103">Importa un file di database nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad41e-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="ad41e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad41e-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ad41e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad41e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad41e-106">Importa un file di database nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad41e-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="ad41e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad41e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad41e-108">Esempio 1: importare un database</span><span class="sxs-lookup"><span data-stu-id="ad41e-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ad41e-109">Questo comando importa un file di database nel database della cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="ad41e-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="ad41e-110">Esempio 2: importare database (con l'esempio filename)</span><span class="sxs-lookup"><span data-stu-id="ad41e-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ad41e-111">Questo comando importa un file di database nel database della cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="ad41e-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="ad41e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad41e-112">PARAMETERS</span></span>

### <span data-ttu-id="ad41e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad41e-113">-AsJob</span></span>
<span data-ttu-id="ad41e-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ad41e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ad41e-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ad41e-115">-ClusterName</span></span>
<span data-ttu-id="ad41e-116">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ad41e-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ad41e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad41e-117">-DefaultProfile</span></span>
<span data-ttu-id="ad41e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad41e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad41e-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ad41e-119">-NoWait</span></span>
<span data-ttu-id="ad41e-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ad41e-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad41e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad41e-121">-PassThru</span></span>
<span data-ttu-id="ad41e-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ad41e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad41e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad41e-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad41e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad41e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad41e-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="ad41e-125">-SasUri</span></span>
<span data-ttu-id="ad41e-126">URI SAS per il BLOB di destinazione da cui importare</span><span class="sxs-lookup"><span data-stu-id="ad41e-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="ad41e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad41e-127">-SubscriptionId</span></span>
<span data-ttu-id="ad41e-128">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad41e-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad41e-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ad41e-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad41e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad41e-130">-Confirm</span></span>
<span data-ttu-id="ad41e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad41e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad41e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad41e-132">-WhatIf</span></span>
<span data-ttu-id="ad41e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad41e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad41e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad41e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad41e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad41e-135">CommonParameters</span></span>
<span data-ttu-id="ad41e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad41e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad41e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad41e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad41e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad41e-138">INPUTS</span></span>

## <span data-ttu-id="ad41e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad41e-139">OUTPUTS</span></span>

### <span data-ttu-id="ad41e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad41e-140">System.Boolean</span></span>

## <span data-ttu-id="ad41e-141">Note</span><span class="sxs-lookup"><span data-stu-id="ad41e-141">NOTES</span></span>

<span data-ttu-id="ad41e-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ad41e-142">ALIASES</span></span>

## <span data-ttu-id="ad41e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad41e-143">RELATED LINKS</span></span>

