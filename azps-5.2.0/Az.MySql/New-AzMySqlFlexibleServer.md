---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329498"
---
# <span data-ttu-id="5b1b2-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5b1b2-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="5b1b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1b2-103">Crea un nuovo server flessibile MySQL</span><span class="sxs-lookup"><span data-stu-id="5b1b2-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="5b1b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b1b2-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b1b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1b2-106">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-106">Creates a new server.</span></span>

## <span data-ttu-id="5b1b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="5b1b2-108">Esempio 1: creare un nuovo server flessibile MySql</span><span class="sxs-lookup"><span data-stu-id="5b1b2-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="5b1b2-109">Esempio 2: creare un nuovo server flessibile MySql con l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="5b1b2-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="5b1b2-110">Creare un server MySql con valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-110">Create MySql server with default values.</span></span>
<span data-ttu-id="5b1b2-111">I valori predefiniti di location sono West US 2, SKU is Standard_B1ms, il livello SKU è Burstable e la dimensione dello spazio di archiviazione è 10GiB.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="5b1b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b1b2-112">PARAMETERS</span></span>

### <span data-ttu-id="5b1b2-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5b1b2-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5b1b2-114">La password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-114">The password of the administrator.</span></span>
<span data-ttu-id="5b1b2-115">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="5b1b2-116">La password deve contenere caratteri da tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="5b1b2-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="5b1b2-117">-AdministratorUserName</span></span>
<span data-ttu-id="5b1b2-118">Nome utente amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-118">Administrator username for the server.</span></span>
<span data-ttu-id="5b1b2-119">Una volta impostato, non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="5b1b2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1b2-120">-AsJob</span></span>
<span data-ttu-id="5b1b2-121">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="5b1b2-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5b1b2-122">-BackupRetentionDay</span></span>
<span data-ttu-id="5b1b2-123">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-123">Backup retention days for the server.</span></span>
<span data-ttu-id="5b1b2-124">Il numero di giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="5b1b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1b2-125">-DefaultProfile</span></span>
<span data-ttu-id="5b1b2-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1b2-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5b1b2-127">-Location</span></span>
<span data-ttu-id="5b1b2-128">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-128">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1b2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b1b2-129">-Name</span></span>
<span data-ttu-id="5b1b2-130">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-130">The name of the server.</span></span>

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

### <span data-ttu-id="5b1b2-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="5b1b2-131">-NoWait</span></span>
<span data-ttu-id="5b1b2-132">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5b1b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="5b1b2-134">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5b1b2-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="5b1b2-135">-Sku</span></span>
<span data-ttu-id="5b1b2-136">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1b2-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5b1b2-137">-SkuTier</span></span>
<span data-ttu-id="5b1b2-138">Livello di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-138">Compute tier of the server.</span></span>
<span data-ttu-id="5b1b2-139">Valori accettati: burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="5b1b2-140">Impostazione predefinita: Burstable.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-140">Default: Burstable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1b2-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5b1b2-141">-StorageInMb</span></span>
<span data-ttu-id="5b1b2-142">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="5b1b2-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b1b2-143">-SubscriptionId</span></span>
<span data-ttu-id="5b1b2-144">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5b1b2-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b1b2-145">-Tag</span></span>
<span data-ttu-id="5b1b2-146">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5b1b2-147">-Versione</span><span class="sxs-lookup"><span data-stu-id="5b1b2-147">-Version</span></span>
<span data-ttu-id="5b1b2-148">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-148">Server version.</span></span>

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

### <span data-ttu-id="5b1b2-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b1b2-149">-Confirm</span></span>
<span data-ttu-id="5b1b2-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1b2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1b2-151">-WhatIf</span></span>
<span data-ttu-id="5b1b2-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1b2-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1b2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1b2-154">CommonParameters</span></span>
<span data-ttu-id="5b1b2-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1b2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1b2-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b1b2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1b2-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b1b2-157">INPUTS</span></span>

## <span data-ttu-id="5b1b2-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b1b2-158">OUTPUTS</span></span>

### <span data-ttu-id="5b1b2-159">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5b1b2-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5b1b2-160">Note</span><span class="sxs-lookup"><span data-stu-id="5b1b2-160">NOTES</span></span>

<span data-ttu-id="5b1b2-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5b1b2-161">ALIASES</span></span>

## <span data-ttu-id="5b1b2-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b1b2-162">RELATED LINKS</span></span>

