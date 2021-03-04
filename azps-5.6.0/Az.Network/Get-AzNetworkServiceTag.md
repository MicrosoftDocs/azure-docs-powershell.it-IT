---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: 4346ec557d149d2555b136cfef15b86770b89dbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006302"
---
# <span data-ttu-id="20837-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="20837-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="20837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20837-102">SYNOPSIS</span></span>
<span data-ttu-id="20837-103">Ottiene l'elenco di risorse di informazioni sui tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="20837-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="20837-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20837-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20837-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20837-105">DESCRIPTION</span></span>
<span data-ttu-id="20837-106">Il cmdlet **Get-AzNetworkServiceTag** ottiene l'elenco delle risorse di informazioni sui tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="20837-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="20837-107">Tieni presente che le informazioni relative all'area geografica di Azure specificate verranno usate come riferimento per la versione (non come filtro basato sulla posizione).</span><span class="sxs-lookup"><span data-stu-id="20837-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="20837-108">Ad esempio, anche se si specifica che si otterrà l'elenco dei tag di servizio con prefissi in tutte le aree geografiche ma limitati al cloud a cui appartiene l'abbonamento (ad esempio Pubblico, Governo degli Stati Uniti, Cina o `-Location eastus2` Germania).</span><span class="sxs-lookup"><span data-stu-id="20837-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="20837-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20837-109">EXAMPLES</span></span>

### <span data-ttu-id="20837-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20837-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="20837-111">Il comando recupera l'elenco delle risorse di informazioni sui tag di servizio e lo archivia in una `serviceTags` variabile.</span><span class="sxs-lookup"><span data-stu-id="20837-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="20837-112">Esempio 2: Ottenere tutti i prefissi di indirizzo per AzureSQL</span><span class="sxs-lookup"><span data-stu-id="20837-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="20837-113">Il primo comando ottiene l'elenco di risorse di informazioni sui tag di servizio e lo archivia in una `serviceTags` variabile.</span><span class="sxs-lookup"><span data-stu-id="20837-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="20837-114">Il secondo comando filtra l'elenco per selezionare le informazioni per Sql.</span><span class="sxs-lookup"><span data-stu-id="20837-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="20837-115">Esempio 3: Ottenere la risorsa di informazioni sul tag di servizio di archiviazione per Stati Uniti occidentali 2</span><span class="sxs-lookup"><span data-stu-id="20837-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="20837-116">Il primo comando ottiene l'elenco di risorse di informazioni sui tag di servizio e lo archivia in una `serviceTags` variabile.</span><span class="sxs-lookup"><span data-stu-id="20837-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="20837-117">I comandi seguenti illustrano vari modi per filtrare l'elenco e selezionare le informazioni sui tag di servizio per l'archiviazione negli Stati Uniti occidentali 2.</span><span class="sxs-lookup"><span data-stu-id="20837-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="20837-118">Esempio 4: Ottenere tutte le risorse sulle informazioni sui tag di servizio globali</span><span class="sxs-lookup"><span data-stu-id="20837-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="20837-119">Il primo comando ottiene l'elenco di risorse di informazioni sui tag di servizio e lo archivia in una `serviceTags` variabile.</span><span class="sxs-lookup"><span data-stu-id="20837-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="20837-120">Il secondo comando filtra l'elenco per selezionare solo quelli senza area geografica impostata.</span><span class="sxs-lookup"><span data-stu-id="20837-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="20837-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20837-121">PARAMETERS</span></span>

### <span data-ttu-id="20837-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20837-122">-DefaultProfile</span></span>
<span data-ttu-id="20837-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20837-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20837-124">-Location</span><span class="sxs-lookup"><span data-stu-id="20837-124">-Location</span></span>
<span data-ttu-id="20837-125">La posizione che verrà usata come riferimento per la versione (non come filtro basato sulla posizione, si otterrà l'elenco di tag di servizio con prefissi in tutte le aree geografiche ma limitati al cloud a cui appartiene l'abbonamento).</span><span class="sxs-lookup"><span data-stu-id="20837-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20837-126">CommonParameters</span></span>
<span data-ttu-id="20837-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20837-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20837-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20837-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="20837-129">INPUTS</span></span>

### <span data-ttu-id="20837-130">System.String</span><span class="sxs-lookup"><span data-stu-id="20837-130">System.String</span></span>

## <span data-ttu-id="20837-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20837-131">OUTPUTS</span></span>

### <span data-ttu-id="20837-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="20837-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="20837-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="20837-133">NOTES</span></span>

## <span data-ttu-id="20837-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20837-134">RELATED LINKS</span></span>
