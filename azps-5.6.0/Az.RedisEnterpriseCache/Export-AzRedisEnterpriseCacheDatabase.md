---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000845"
---
# <span data-ttu-id="ddc76-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ddc76-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ddc76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc76-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc76-103">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ddc76-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="ddc76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddc76-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ddc76-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddc76-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc76-106">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ddc76-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="ddc76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddc76-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc76-108">Esempio 1: Esportare un database</span><span class="sxs-lookup"><span data-stu-id="ddc76-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ddc76-109">Questo comando esporta il database della cache dell'organizzazione di Redis denominata MyCache in un file di database.</span><span class="sxs-lookup"><span data-stu-id="ddc76-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="ddc76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddc76-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc76-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddc76-111">-AsJob</span></span>
<span data-ttu-id="ddc76-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ddc76-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ddc76-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ddc76-113">-ClusterName</span></span>
<span data-ttu-id="ddc76-114">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ddc76-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ddc76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc76-115">-DefaultProfile</span></span>
<span data-ttu-id="ddc76-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc76-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddc76-117">-NoWait</span></span>
<span data-ttu-id="ddc76-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ddc76-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddc76-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddc76-119">-PassThru</span></span>
<span data-ttu-id="ddc76-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="ddc76-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ddc76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc76-121">-ResourceGroupName</span></span>
<span data-ttu-id="ddc76-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddc76-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddc76-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="ddc76-123">-SasUri</span></span>
<span data-ttu-id="ddc76-124">Uri della firma di accesso condiviso per la directory di destinazione in cui esportare</span><span class="sxs-lookup"><span data-stu-id="ddc76-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="ddc76-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddc76-125">-SubscriptionId</span></span>
<span data-ttu-id="ddc76-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc76-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ddc76-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ddc76-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ddc76-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddc76-128">-Confirm</span></span>
<span data-ttu-id="ddc76-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc76-130">-WhatIf</span></span>
<span data-ttu-id="ddc76-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddc76-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc76-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddc76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc76-133">CommonParameters</span></span>
<span data-ttu-id="ddc76-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc76-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddc76-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc76-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddc76-136">INPUTS</span></span>

## <span data-ttu-id="ddc76-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddc76-137">OUTPUTS</span></span>

### <span data-ttu-id="ddc76-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddc76-138">System.Boolean</span></span>

## <span data-ttu-id="ddc76-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddc76-139">NOTES</span></span>

<span data-ttu-id="ddc76-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ddc76-140">ALIASES</span></span>

## <span data-ttu-id="ddc76-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddc76-141">RELATED LINKS</span></span>

