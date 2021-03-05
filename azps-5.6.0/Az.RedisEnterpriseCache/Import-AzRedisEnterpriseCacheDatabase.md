---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000781"
---
# <span data-ttu-id="da419-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="da419-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="da419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da419-102">SYNOPSIS</span></span>
<span data-ttu-id="da419-103">Importa un file di database nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da419-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="da419-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da419-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="da419-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da419-105">DESCRIPTION</span></span>
<span data-ttu-id="da419-106">Importa un file di database nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da419-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="da419-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da419-107">EXAMPLES</span></span>

### <span data-ttu-id="da419-108">Esempio 1: Importare un database</span><span class="sxs-lookup"><span data-stu-id="da419-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="da419-109">Questo comando importa un file di database nel database della cache di Redis Enterprise denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="da419-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="da419-110">Esempio 2: Importare il database (usando il nome file di esempio)</span><span class="sxs-lookup"><span data-stu-id="da419-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="da419-111">Questo comando importa un file di database nel database della cache di Redis Enterprise denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="da419-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="da419-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da419-112">PARAMETERS</span></span>

### <span data-ttu-id="da419-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da419-113">-AsJob</span></span>
<span data-ttu-id="da419-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="da419-114">Run the command as a job</span></span>

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

### <span data-ttu-id="da419-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="da419-115">-ClusterName</span></span>
<span data-ttu-id="da419-116">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="da419-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="da419-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da419-117">-DefaultProfile</span></span>
<span data-ttu-id="da419-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da419-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da419-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da419-119">-NoWait</span></span>
<span data-ttu-id="da419-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="da419-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da419-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da419-121">-PassThru</span></span>
<span data-ttu-id="da419-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="da419-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da419-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da419-123">-ResourceGroupName</span></span>
<span data-ttu-id="da419-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da419-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="da419-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="da419-125">-SasUri</span></span>
<span data-ttu-id="da419-126">Uri di firma di accesso condiviso per il BLOB di destinazione da cui importare</span><span class="sxs-lookup"><span data-stu-id="da419-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="da419-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da419-127">-SubscriptionId</span></span>
<span data-ttu-id="da419-128">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="da419-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="da419-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="da419-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da419-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da419-130">-Confirm</span></span>
<span data-ttu-id="da419-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da419-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da419-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da419-132">-WhatIf</span></span>
<span data-ttu-id="da419-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da419-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da419-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da419-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da419-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da419-135">CommonParameters</span></span>
<span data-ttu-id="da419-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da419-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da419-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da419-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da419-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="da419-138">INPUTS</span></span>

## <span data-ttu-id="da419-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da419-139">OUTPUTS</span></span>

### <span data-ttu-id="da419-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da419-140">System.Boolean</span></span>

## <span data-ttu-id="da419-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="da419-141">NOTES</span></span>

<span data-ttu-id="da419-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da419-142">ALIASES</span></span>

## <span data-ttu-id="da419-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da419-143">RELATED LINKS</span></span>

