---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023313"
---
# <span data-ttu-id="9666d-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="9666d-101">Get-AzsBackup</span></span>

## <span data-ttu-id="9666d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9666d-102">SYNOPSIS</span></span>
<span data-ttu-id="9666d-103">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9666d-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="9666d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9666d-104">SYNTAX</span></span>

### <span data-ttu-id="9666d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9666d-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9666d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9666d-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9666d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9666d-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9666d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9666d-108">DESCRIPTION</span></span>
<span data-ttu-id="9666d-109">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9666d-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="9666d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9666d-110">EXAMPLES</span></span>

### <span data-ttu-id="9666d-111">Esempio 1: backup elenco</span><span class="sxs-lookup"><span data-stu-id="9666d-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="9666d-112">Ottenere informazioni sbout tutti i backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="9666d-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="9666d-113">Esempio 2: ottenere un backup specifico</span><span class="sxs-lookup"><span data-stu-id="9666d-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="9666d-114">Ottenere informazioni per il backup dello stack di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9666d-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="9666d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9666d-115">PARAMETERS</span></span>

### <span data-ttu-id="9666d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9666d-116">-DefaultProfile</span></span>
<span data-ttu-id="9666d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9666d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9666d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9666d-118">-InputObject</span></span>
<span data-ttu-id="9666d-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9666d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9666d-120">-Location</span></span>
<span data-ttu-id="9666d-121">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="9666d-121">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9666d-122">-Name</span></span>
<span data-ttu-id="9666d-123">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="9666d-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9666d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9666d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9666d-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="9666d-126">-Skip</span></span>
<span data-ttu-id="9666d-127">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="9666d-127">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9666d-128">-SubscriptionId</span></span>
<span data-ttu-id="9666d-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9666d-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9666d-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9666d-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-131">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9666d-131">-Top</span></span>
<span data-ttu-id="9666d-132">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="9666d-132">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9666d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9666d-133">CommonParameters</span></span>
<span data-ttu-id="9666d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9666d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9666d-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9666d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9666d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9666d-136">INPUTS</span></span>

### <span data-ttu-id="9666d-137">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9666d-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="9666d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9666d-138">OUTPUTS</span></span>

### <span data-ttu-id="9666d-139">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="9666d-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="9666d-140">Note</span><span class="sxs-lookup"><span data-stu-id="9666d-140">NOTES</span></span>

<span data-ttu-id="9666d-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9666d-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9666d-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9666d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9666d-143">INPUTOBJECT <IBackupAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9666d-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9666d-144">`[Backup <String>]`: Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="9666d-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="9666d-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9666d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9666d-146">`[Location <String>]`: Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="9666d-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="9666d-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9666d-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9666d-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9666d-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9666d-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9666d-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9666d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9666d-150">RELATED LINKS</span></span>

