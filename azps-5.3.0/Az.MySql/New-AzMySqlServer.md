---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474041"
---
# <span data-ttu-id="71dd5-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="71dd5-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="71dd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="71dd5-103">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-103">Creates a new server.</span></span>

## <span data-ttu-id="71dd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71dd5-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71dd5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="71dd5-106">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-106">Creates a new server.</span></span>

## <span data-ttu-id="71dd5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="71dd5-108">Esempio 1: creare un nuovo server MySql</span><span class="sxs-lookup"><span data-stu-id="71dd5-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="71dd5-109">Questi cmdlet creano un nuovo server MySql.</span><span class="sxs-lookup"><span data-stu-id="71dd5-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="71dd5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71dd5-110">PARAMETERS</span></span>

### <span data-ttu-id="71dd5-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="71dd5-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="71dd5-112">La password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="71dd5-112">The password of the administrator.</span></span>
<span data-ttu-id="71dd5-113">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="71dd5-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="71dd5-114">La password deve contenere caratteri da tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="71dd5-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="71dd5-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="71dd5-115">-AdministratorUserName</span></span>
<span data-ttu-id="71dd5-116">Nome utente amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-116">Administrator username for the server.</span></span>
<span data-ttu-id="71dd5-117">Una volta impostato, non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="71dd5-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="71dd5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71dd5-118">-AsJob</span></span>
<span data-ttu-id="71dd5-119">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="71dd5-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="71dd5-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="71dd5-120">-BackupRetentionDay</span></span>
<span data-ttu-id="71dd5-121">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-121">Backup retention days for the server.</span></span>
<span data-ttu-id="71dd5-122">Il numero di giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="71dd5-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="71dd5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71dd5-123">-DefaultProfile</span></span>
<span data-ttu-id="71dd5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71dd5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71dd5-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="71dd5-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="71dd5-126">Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="71dd5-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="71dd5-127">-Location</span></span>
<span data-ttu-id="71dd5-128">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71dd5-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="71dd5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="71dd5-129">-Name</span></span>
<span data-ttu-id="71dd5-130">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-130">The name of the server.</span></span>

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

### <span data-ttu-id="71dd5-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="71dd5-131">-NoWait</span></span>
<span data-ttu-id="71dd5-132">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="71dd5-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="71dd5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71dd5-133">-ResourceGroupName</span></span>
<span data-ttu-id="71dd5-134">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="71dd5-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="71dd5-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="71dd5-135">-Sku</span></span>
<span data-ttu-id="71dd5-136">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="71dd5-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="71dd5-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="71dd5-137">-SslEnforcement</span></span>
<span data-ttu-id="71dd5-138">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="71dd5-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="71dd5-139">-StorageAutogrow</span></span>
<span data-ttu-id="71dd5-140">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="71dd5-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="71dd5-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="71dd5-141">-StorageInMb</span></span>
<span data-ttu-id="71dd5-142">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="71dd5-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71dd5-143">-SubscriptionId</span></span>
<span data-ttu-id="71dd5-144">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="71dd5-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="71dd5-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="71dd5-145">-Tag</span></span>
<span data-ttu-id="71dd5-146">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="71dd5-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="71dd5-147">-Versione</span><span class="sxs-lookup"><span data-stu-id="71dd5-147">-Version</span></span>
<span data-ttu-id="71dd5-148">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="71dd5-148">Server version.</span></span>

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

### <span data-ttu-id="71dd5-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71dd5-149">-Confirm</span></span>
<span data-ttu-id="71dd5-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71dd5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71dd5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71dd5-151">-WhatIf</span></span>
<span data-ttu-id="71dd5-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71dd5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71dd5-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71dd5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71dd5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71dd5-154">CommonParameters</span></span>
<span data-ttu-id="71dd5-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71dd5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71dd5-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71dd5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71dd5-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71dd5-157">INPUTS</span></span>

## <span data-ttu-id="71dd5-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71dd5-158">OUTPUTS</span></span>

### <span data-ttu-id="71dd5-159">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="71dd5-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="71dd5-160">Note</span><span class="sxs-lookup"><span data-stu-id="71dd5-160">NOTES</span></span>

<span data-ttu-id="71dd5-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71dd5-161">ALIASES</span></span>

## <span data-ttu-id="71dd5-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71dd5-162">RELATED LINKS</span></span>

