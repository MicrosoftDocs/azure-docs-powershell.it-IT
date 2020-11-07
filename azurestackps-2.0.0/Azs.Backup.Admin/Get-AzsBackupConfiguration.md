---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864061"
---
# <span data-ttu-id="77781-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="77781-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="77781-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77781-102">SYNOPSIS</span></span>
<span data-ttu-id="77781-103">Restituisce una posizione di backup specifica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="77781-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="77781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77781-104">SYNTAX</span></span>

### <span data-ttu-id="77781-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77781-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77781-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="77781-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="77781-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="77781-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="77781-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77781-108">DESCRIPTION</span></span>
<span data-ttu-id="77781-109">Restituisce una posizione di backup specifica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="77781-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="77781-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77781-110">EXAMPLES</span></span>

### <span data-ttu-id="77781-111">Esempio 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="77781-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="77781-112">Ottenere la configurazione di backup dello stack Azure.</span><span class="sxs-lookup"><span data-stu-id="77781-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="77781-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77781-113">PARAMETERS</span></span>

### <span data-ttu-id="77781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77781-114">-DefaultProfile</span></span>
<span data-ttu-id="77781-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77781-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77781-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77781-116">-InputObject</span></span>
<span data-ttu-id="77781-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="77781-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="77781-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="77781-118">-Location</span></span>
<span data-ttu-id="77781-119">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="77781-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="77781-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77781-120">-ResourceGroupName</span></span>
<span data-ttu-id="77781-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77781-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="77781-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="77781-122">-Skip</span></span>
<span data-ttu-id="77781-123">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="77781-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="77781-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77781-124">-SubscriptionId</span></span>
<span data-ttu-id="77781-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77781-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="77781-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="77781-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="77781-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="77781-127">-Top</span></span>
<span data-ttu-id="77781-128">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="77781-128">OData top parameter.</span></span>

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

### <span data-ttu-id="77781-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77781-129">CommonParameters</span></span>
<span data-ttu-id="77781-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77781-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77781-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77781-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77781-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77781-132">INPUTS</span></span>

### <span data-ttu-id="77781-133">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="77781-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="77781-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77781-134">OUTPUTS</span></span>

### <span data-ttu-id="77781-135">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="77781-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="77781-136">Note</span><span class="sxs-lookup"><span data-stu-id="77781-136">NOTES</span></span>

<span data-ttu-id="77781-137">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="77781-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77781-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="77781-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="77781-139">INPUTOBJECT <IBackupAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="77781-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="77781-140">`[Backup <String>]`: Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="77781-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="77781-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="77781-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="77781-142">`[Location <String>]`: Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="77781-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="77781-143">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77781-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="77781-144">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77781-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="77781-145">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="77781-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="77781-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77781-146">RELATED LINKS</span></span>

