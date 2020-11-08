---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199828"
---
# <span data-ttu-id="ec4c6-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec4c6-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="ec4c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4c6-103">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-103">Creates a new server.</span></span>

## <span data-ttu-id="ec4c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec4c6-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec4c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec4c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4c6-106">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-106">Creates a new server.</span></span>

## <span data-ttu-id="ec4c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec4c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ec4c6-108">Esempio 1: creare un nuovo server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ec4c6-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ec4c6-109">Questi cmdlet creano un nuovo server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="ec4c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec4c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ec4c6-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ec4c6-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ec4c6-112">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-112">The location the resource resides in.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ec4c6-113">-AdministratorUserName</span></span>
<span data-ttu-id="ec4c6-114">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ec4c6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec4c6-115">-AsJob</span></span>
<span data-ttu-id="ec4c6-116">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="ec4c6-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ec4c6-117">-BackupRetentionDay</span></span>
<span data-ttu-id="ec4c6-118">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-118">Backup retention days for the server.</span></span>
<span data-ttu-id="ec4c6-119">Il numero di giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-119">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4c6-120">-DefaultProfile</span></span>
<span data-ttu-id="ec4c6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4c6-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ec4c6-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="ec4c6-123">Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ec4c6-124">-Location</span></span>
<span data-ttu-id="ec4c6-125">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ec4c6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec4c6-126">-Name</span></span>
<span data-ttu-id="ec4c6-127">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-127">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ec4c6-128">-NoWait</span></span>
<span data-ttu-id="ec4c6-129">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ec4c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="ec4c6-131">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ec4c6-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="ec4c6-132">-Sku</span></span>
<span data-ttu-id="ec4c6-133">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ec4c6-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ec4c6-134">-SslEnforcement</span></span>
<span data-ttu-id="ec4c6-135">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="ec4c6-136">-StorageAutogrow</span></span>
<span data-ttu-id="ec4c6-137">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ec4c6-138">-StorageInMb</span></span>
<span data-ttu-id="ec4c6-139">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-139">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec4c6-140">-SubscriptionId</span></span>
<span data-ttu-id="ec4c6-141">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ec4c6-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec4c6-142">-Tag</span></span>
<span data-ttu-id="ec4c6-143">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-143">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-144">-Versione</span><span class="sxs-lookup"><span data-stu-id="ec4c6-144">-Version</span></span>
<span data-ttu-id="ec4c6-145">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4c6-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec4c6-146">-Confirm</span></span>
<span data-ttu-id="ec4c6-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4c6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4c6-148">-WhatIf</span></span>
<span data-ttu-id="ec4c6-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4c6-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4c6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4c6-151">CommonParameters</span></span>
<span data-ttu-id="ec4c6-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4c6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4c6-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec4c6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4c6-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec4c6-154">INPUTS</span></span>

## <span data-ttu-id="ec4c6-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec4c6-155">OUTPUTS</span></span>

### <span data-ttu-id="ec4c6-156">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ec4c6-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ec4c6-157">Note</span><span class="sxs-lookup"><span data-stu-id="ec4c6-157">NOTES</span></span>

<span data-ttu-id="ec4c6-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ec4c6-158">ALIASES</span></span>

## <span data-ttu-id="ec4c6-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec4c6-159">RELATED LINKS</span></span>

