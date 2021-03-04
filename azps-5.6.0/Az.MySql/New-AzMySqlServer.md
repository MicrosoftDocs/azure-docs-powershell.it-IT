---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 2ae1e3e92a4118cb6d629f82a837b161ac012724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962814"
---
# <span data-ttu-id="3c2c5-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="3c2c5-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="3c2c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2c5-103">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-103">Creates a new server.</span></span>

## <span data-ttu-id="3c2c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c2c5-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c2c5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c2c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3c2c5-106">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-106">Creates a new server.</span></span>

## <span data-ttu-id="3c2c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c2c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3c2c5-108">Esempio 1: Creare un nuovo server MySql</span><span class="sxs-lookup"><span data-stu-id="3c2c5-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c2c5-109">Questi cmdlet creano un nuovo server MySql.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="3c2c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c2c5-110">PARAMETERS</span></span>

### <span data-ttu-id="3c2c5-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3c2c5-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3c2c5-112">Password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-112">The password of the administrator.</span></span>
<span data-ttu-id="3c2c5-113">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="3c2c5-114">La password deve contenere caratteri di tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole inglesi, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="3c2c5-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="3c2c5-115">-AdministratorUserName</span></span>
<span data-ttu-id="3c2c5-116">Nome utente dell'amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-116">Administrator username for the server.</span></span>
<span data-ttu-id="3c2c5-117">Una volta impostata, non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="3c2c5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c2c5-118">-AsJob</span></span>
<span data-ttu-id="3c2c5-119">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="3c2c5-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="3c2c5-120">-BackupRetentionDay</span></span>
<span data-ttu-id="3c2c5-121">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-121">Backup retention days for the server.</span></span>
<span data-ttu-id="3c2c5-122">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="3c2c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2c5-123">-DefaultProfile</span></span>
<span data-ttu-id="3c2c5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2c5-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="3c2c5-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="3c2c5-126">Abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2c5-127">-Location</span><span class="sxs-lookup"><span data-stu-id="3c2c5-127">-Location</span></span>
<span data-ttu-id="3c2c5-128">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3c2c5-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3c2c5-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="3c2c5-130">Impostare la versione minima di TLS per le connessioni al server quando è abilitato SSL.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="3c2c5-131">Il valore predefinito è TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2c5-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3c2c5-132">-Name</span></span>
<span data-ttu-id="3c2c5-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-133">The name of the server.</span></span>

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

### <span data-ttu-id="3c2c5-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c2c5-134">-NoWait</span></span>
<span data-ttu-id="3c2c5-135">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="3c2c5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2c5-136">-ResourceGroupName</span></span>
<span data-ttu-id="3c2c5-137">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3c2c5-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="3c2c5-138">-Sku</span></span>
<span data-ttu-id="3c2c5-139">Il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="3c2c5-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="3c2c5-140">-SslEnforcement</span></span>
<span data-ttu-id="3c2c5-141">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-141">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2c5-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="3c2c5-142">-StorageAutogrow</span></span>
<span data-ttu-id="3c2c5-143">Abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-143">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2c5-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="3c2c5-144">-StorageInMb</span></span>
<span data-ttu-id="3c2c5-145">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="3c2c5-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c2c5-146">-SubscriptionId</span></span>
<span data-ttu-id="3c2c5-147">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3c2c5-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c2c5-148">-Tag</span></span>
<span data-ttu-id="3c2c5-149">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3c2c5-150">-Version</span><span class="sxs-lookup"><span data-stu-id="3c2c5-150">-Version</span></span>
<span data-ttu-id="3c2c5-151">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-151">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2c5-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c2c5-152">-Confirm</span></span>
<span data-ttu-id="3c2c5-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2c5-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2c5-154">-WhatIf</span></span>
<span data-ttu-id="3c2c5-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c2c5-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2c5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2c5-157">CommonParameters</span></span>
<span data-ttu-id="3c2c5-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2c5-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2c5-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c2c5-160">INPUTS</span></span>

## <span data-ttu-id="3c2c5-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c2c5-161">OUTPUTS</span></span>

### <span data-ttu-id="3c2c5-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="3c2c5-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3c2c5-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c2c5-163">NOTES</span></span>

<span data-ttu-id="3c2c5-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3c2c5-164">ALIASES</span></span>

## <span data-ttu-id="3c2c5-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c2c5-165">RELATED LINKS</span></span>

