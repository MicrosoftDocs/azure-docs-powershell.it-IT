---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/get-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: 5523dd35ae91b9fea7db5f2451401793cb6059c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863978"
---
# <span data-ttu-id="d7961-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d7961-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="d7961-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7961-102">SYNOPSIS</span></span>
<span data-ttu-id="d7961-103">Ottenere un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="d7961-103">Get a specific gallery item.</span></span>

## <span data-ttu-id="d7961-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7961-104">SYNTAX</span></span>

### <span data-ttu-id="d7961-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7961-105">List (Default)</span></span>
```
Get-AzsGalleryItem [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7961-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d7961-106">Get</span></span>
```
Get-AzsGalleryItem -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="d7961-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7961-107">GetViaIdentity</span></span>
```
Get-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d7961-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7961-108">DESCRIPTION</span></span>
<span data-ttu-id="d7961-109">Ottenere un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="d7961-109">Get a specific gallery item.</span></span>

## <span data-ttu-id="d7961-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7961-110">EXAMPLES</span></span>

### <span data-ttu-id="d7961-111">Esempio 1: Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d7961-111">Example 1: Get-AzsGalleryItem</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM
```

<span data-ttu-id="d7961-112">Ottiene l'elemento della raccolta in base al nome.</span><span class="sxs-lookup"><span data-stu-id="d7961-112">Gets the gallery item by name.</span></span>

### <span data-ttu-id="d7961-113">Esempio 2: elementi della raccolta elenchi</span><span class="sxs-lookup"><span data-stu-id="d7961-113">Example 2: List Gallery Items</span></span>
```powershell
PS C:\> Get-AzsGalleryItem

Name                                       Publisher PublisherDisplayName  ItemName                  ItemDisplayName
----                                       --------- --------------------  --------                  ---------------
Canonical.UbuntuServer1804LTS-ARM.1.0.3    Canonical Canonical             UbuntuServer1804LTS-ARM   Ubuntu Server 1...
Microsoft.AddOnRP-WindowsServer.1.1910.3   Microsoft Microsoft             AddOnRP-WindowsServer     Microsoft Azure...
Microsoft.AdminOffer.6.0.0                 Microsoft Microsoft Corporation AdminOffer                Offer
Microsoft.AvailabilitySet-ARM.1.0.1        Microsoft Microsoft             AvailabilitySet-ARM       Availability Set
Microsoft.Connection-ARM.1.2.2             Microsoft Microsoft             Connection-ARM            Connection
Microsoft.CustomScriptExtension-arm.2.0.10 Microsoft Microsoft Corp.       CustomScriptExtension-arm Custom Script E...
Microsoft.DSC-arm.2.0.7                    Microsoft Microsoft Corp.       DSC-arm                   PowerShell Desi...
Microsoft.DnsZone-ARM.1.0.1                Microsoft Microsoft             DnsZone-ARM               DNS zone
Microsoft.Image-ARM.1.0.2                  Microsoft Microsoft             Image-ARM                 Image
Microsoft.KeyVault.1.0.14                  Microsoft Microsoft             KeyVault                  Key Vault
Microsoft.LoadBalancer-ARM.1.0.2           Microsoft Microsoft             LoadBalancer-ARM          Load Balancer
Microsoft.LocalNetworkGateway-ARM.1.0.3    Microsoft Microsoft             LocalNetworkGateway-ARM   Local network g...
Microsoft.ManagedDisk-ARM.1.0.2            Microsoft Microsoft             ManagedDisk-ARM           Managed Disks
Microsoft.NetworkInterface-ARM.1.0.4       Microsoft Microsoft             NetworkInterface-ARM      Network interface
Microsoft.NetworkSecurityGroup-ARM.1.0.4   Microsoft Microsoft             NetworkSecurityGroup-ARM  Network securit...
Microsoft.Offer.6.0.0                      Microsoft Microsoft Corporation Offer                     Offer
Microsoft.Plan.6.0.0                       Microsoft Microsoft Corporation Plan                      Plan
Microsoft.PublicIPAddress-ARM.1.0.2        Microsoft Microsoft             PublicIPAddress-ARM       Public IP address
Microsoft.PublicIPPool-ARM.1.0.0           Microsoft Microsoft             PublicIPPool-ARM          Public IP pool
Microsoft.ResourceGroup.6.0.0              Microsoft Microsoft             ResourceGroup             Resource group
Microsoft.RouteTable-ARM.1.0.2             Microsoft Microsoft             RouteTable-ARM            Route table
Microsoft.ScaleUnitNode-ARM.1.0.0          Microsoft Microsoft             ScaleUnitNode-ARM         Scale Unit Node
Microsoft.Snapshot-ARM.1.0.2               Microsoft Microsoft             Snapshot-ARM              Snapshot
Microsoft.StorageAccount-ARM.101.0.1       Microsoft Microsoft             StorageAccount-ARM        Storage account
Microsoft.StorageAccount-ARM.1.0.3         Microsoft Microsoft             StorageAccount-ARM        Storage account...
Microsoft.Template.6.0.0                   Microsoft Microsoft             Template                  Template deploy...
Microsoft.TenantSubscription.6.0.0         Microsoft Microsoft Corporation TenantSubscription        Subscription
Microsoft.VirtualMachine-ARM.1.0.2         Microsoft Microsoft             VirtualMachine-ARM        Virtual machine
Microsoft.VirtualNetwork-ARM.1.0.4         Microsoft Microsoft             VirtualNetwork-ARM        Virtual network
Microsoft.VirtualNetworkGateway-ARM.1.0.3  Microsoft Microsoft             VirtualNetworkGateway-ARM Virtual network...
microsoft.antimalware-windows-arm.1.0.0    microsoft Microsoft Corp.       antimalware-windows-arm   Microsoft Antim...
microsoft.custom-script2-linux-arm.3.0.0   microsoft Microsoft Corp.       custom-script2-linux-arm  Custom Script F...
microsoft.custom-script-linux-arm.2.0.50   microsoft Microsoft Corp.       custom-script-linux-arm   Custom Script F...
microsoft.docker-arm.1.1.0                 microsoft Microsoft             docker-arm                Docker
microsoft.vmss.7.1.7                       microsoft Microsoft             vmss                      Virtual machine...

```

<span data-ttu-id="d7961-114">Elenca tutti gli elementi disponibili nella raccolta stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7961-114">Lists all the items available in the Azure Stack gallery.</span></span>

## <span data-ttu-id="d7961-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7961-115">PARAMETERS</span></span>

### <span data-ttu-id="d7961-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7961-116">-DefaultProfile</span></span>
<span data-ttu-id="d7961-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7961-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7961-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7961-118">-InputObject</span></span>
<span data-ttu-id="d7961-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d7961-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d7961-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7961-120">-Name</span></span>
<span data-ttu-id="d7961-121">Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d7961-121">Identity of the gallery item.</span></span>
<span data-ttu-id="d7961-122">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="d7961-122">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d7961-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7961-123">-PassThru</span></span>
<span data-ttu-id="d7961-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="d7961-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d7961-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7961-125">-SubscriptionId</span></span>
<span data-ttu-id="d7961-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d7961-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7961-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d7961-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d7961-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7961-128">CommonParameters</span></span>
<span data-ttu-id="d7961-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7961-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7961-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7961-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7961-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7961-131">INPUTS</span></span>

### <span data-ttu-id="d7961-132">Microsoft. Azure. PowerShell. Cmdlets. gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="d7961-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="d7961-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7961-133">OUTPUTS</span></span>

### <span data-ttu-id="d7961-134">Microsoft. Azure. PowerShell. Cmdlets. gallery. Models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d7961-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="d7961-135">Note</span><span class="sxs-lookup"><span data-stu-id="d7961-135">NOTES</span></span>

<span data-ttu-id="d7961-136">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d7961-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7961-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7961-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d7961-138">INPUTOBJECT <IGalleryIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d7961-138">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7961-139">`[GalleryItemName <String>]`: Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d7961-139">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="d7961-140">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="d7961-140">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="d7961-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d7961-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7961-142">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d7961-142">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d7961-143">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d7961-143">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d7961-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7961-144">RELATED LINKS</span></span>

