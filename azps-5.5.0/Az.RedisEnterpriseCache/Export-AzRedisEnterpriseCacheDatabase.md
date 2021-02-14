---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183783"
---
# <span data-ttu-id="249b5-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="249b5-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="249b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="249b5-102">SYNOPSIS</span></span>
<span data-ttu-id="249b5-103">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="249b5-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="249b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="249b5-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="249b5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="249b5-105">DESCRIPTION</span></span>
<span data-ttu-id="249b5-106">Esporta un file di database dal database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="249b5-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="249b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="249b5-107">EXAMPLES</span></span>

### <span data-ttu-id="249b5-108">Esempio 1: Esportare un database</span><span class="sxs-lookup"><span data-stu-id="249b5-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="249b5-109">Questo comando esporta il database della cache dell'organizzazione di Redis denominata MyCache in un file di database.</span><span class="sxs-lookup"><span data-stu-id="249b5-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="249b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="249b5-110">PARAMETERS</span></span>

### <span data-ttu-id="249b5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="249b5-111">-AsJob</span></span>
<span data-ttu-id="249b5-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="249b5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="249b5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="249b5-113">-ClusterName</span></span>
<span data-ttu-id="249b5-114">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="249b5-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="249b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249b5-115">-DefaultProfile</span></span>
<span data-ttu-id="249b5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="249b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="249b5-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="249b5-117">-NoWait</span></span>
<span data-ttu-id="249b5-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="249b5-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="249b5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="249b5-119">-PassThru</span></span>
<span data-ttu-id="249b5-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="249b5-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="249b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="249b5-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="249b5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="249b5-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="249b5-123">-SasUri</span></span>
<span data-ttu-id="249b5-124">Uri della firma di accesso condiviso per la directory di destinazione in cui esportare</span><span class="sxs-lookup"><span data-stu-id="249b5-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="249b5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="249b5-125">-SubscriptionId</span></span>
<span data-ttu-id="249b5-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="249b5-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="249b5-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="249b5-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="249b5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="249b5-128">-Confirm</span></span>
<span data-ttu-id="249b5-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="249b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="249b5-130">-WhatIf</span></span>
<span data-ttu-id="249b5-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="249b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="249b5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="249b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="249b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249b5-133">CommonParameters</span></span>
<span data-ttu-id="249b5-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="249b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249b5-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="249b5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249b5-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="249b5-136">INPUTS</span></span>

## <span data-ttu-id="249b5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="249b5-137">OUTPUTS</span></span>

### <span data-ttu-id="249b5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="249b5-138">System.Boolean</span></span>

## <span data-ttu-id="249b5-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="249b5-139">NOTES</span></span>

<span data-ttu-id="249b5-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="249b5-140">ALIASES</span></span>

## <span data-ttu-id="249b5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="249b5-141">RELATED LINKS</span></span>

