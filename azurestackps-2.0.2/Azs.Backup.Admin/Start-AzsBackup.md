---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030496"
---
# <span data-ttu-id="db69c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="db69c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="db69c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db69c-102">SYNOPSIS</span></span>
<span data-ttu-id="db69c-103">Eseguire il backup di una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="db69c-103">Back up a specific location.</span></span>

## <span data-ttu-id="db69c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db69c-104">SYNTAX</span></span>

### <span data-ttu-id="db69c-105">Crea (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db69c-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db69c-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db69c-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db69c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db69c-107">DESCRIPTION</span></span>
<span data-ttu-id="db69c-108">Eseguire il backup di una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="db69c-108">Back up a specific location.</span></span>

## <span data-ttu-id="db69c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db69c-109">EXAMPLES</span></span>

### <span data-ttu-id="db69c-110">Esempio 1: avviare il backup di azurestack</span><span class="sxs-lookup"><span data-stu-id="db69c-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="db69c-111">Avviare un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="db69c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="db69c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db69c-112">PARAMETERS</span></span>

### <span data-ttu-id="db69c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db69c-113">-AsJob</span></span>
<span data-ttu-id="db69c-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="db69c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="db69c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db69c-115">-DefaultProfile</span></span>
<span data-ttu-id="db69c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db69c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db69c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db69c-117">-InputObject</span></span>
<span data-ttu-id="db69c-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="db69c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="db69c-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db69c-119">-Location</span></span>
<span data-ttu-id="db69c-120">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="db69c-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db69c-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="db69c-121">-NoWait</span></span>
<span data-ttu-id="db69c-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="db69c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="db69c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db69c-123">-ResourceGroupName</span></span>
<span data-ttu-id="db69c-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db69c-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db69c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db69c-125">-SubscriptionId</span></span>
<span data-ttu-id="db69c-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db69c-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db69c-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="db69c-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db69c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db69c-128">-Confirm</span></span>
<span data-ttu-id="db69c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db69c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db69c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db69c-130">-WhatIf</span></span>
<span data-ttu-id="db69c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db69c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db69c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db69c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db69c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db69c-133">CommonParameters</span></span>
<span data-ttu-id="db69c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db69c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db69c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db69c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db69c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db69c-136">INPUTS</span></span>

### <span data-ttu-id="db69c-137">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="db69c-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="db69c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db69c-138">OUTPUTS</span></span>

### <span data-ttu-id="db69c-139">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="db69c-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="db69c-140">Note</span><span class="sxs-lookup"><span data-stu-id="db69c-140">NOTES</span></span>

<span data-ttu-id="db69c-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="db69c-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db69c-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db69c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="db69c-143">INPUTOBJECT <IBackupAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="db69c-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db69c-144">`[Backup <String>]`: Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="db69c-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="db69c-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="db69c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db69c-146">`[Location <String>]`: Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="db69c-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="db69c-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db69c-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="db69c-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db69c-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db69c-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="db69c-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="db69c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db69c-150">RELATED LINKS</span></span>

