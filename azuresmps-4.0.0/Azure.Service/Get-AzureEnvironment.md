---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029814"
---
# <span data-ttu-id="cb64e-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb64e-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="cb64e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb64e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb64e-103">Ottiene gli ambienti Azure</span><span class="sxs-lookup"><span data-stu-id="cb64e-103">Gets Azure environments</span></span>

## <span data-ttu-id="cb64e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb64e-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb64e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb64e-105">DESCRIPTION</span></span>
<span data-ttu-id="cb64e-106">Il cmdlet **Get-AzureEnvironment** ottiene gli ambienti Azure disponibili per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cb64e-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="cb64e-107">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="cb64e-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="cb64e-108">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="cb64e-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="cb64e-109">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb64e-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="cb64e-110">Il cmdlet **Get-AzureEnvironment** ottiene gli ambienti dal file di dati dell'abbonamento, non da Azure.</span><span class="sxs-lookup"><span data-stu-id="cb64e-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="cb64e-111">Se il file di dati dell'abbonamento non è aggiornato, eseguire il cmdlet **Add-AzureAccount** o **Import-PublishSettingsFile** per aggiornarlo.</span><span class="sxs-lookup"><span data-stu-id="cb64e-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="cb64e-112">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb64e-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cb64e-113">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cb64e-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="cb64e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb64e-114">EXAMPLES</span></span>

### <span data-ttu-id="cb64e-115">Esempio 1: ottenere tutti gli ambienti</span><span class="sxs-lookup"><span data-stu-id="cb64e-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="cb64e-116">Questo comando consente di ottenere tutti gli ambienti disponibili per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cb64e-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="cb64e-117">Esempio 2: ottenere un ambiente per nome</span><span class="sxs-lookup"><span data-stu-id="cb64e-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="cb64e-118">Questo esempio restituisce l'ambiente AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="cb64e-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="cb64e-119">Esempio 3: ottenere tutte le proprietà di tutti gli ambienti</span><span class="sxs-lookup"><span data-stu-id="cb64e-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="cb64e-120">Questo comando consente di ottenere tutte le proprietà di tutti gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="cb64e-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="cb64e-121">Il comando usa il cmdlet **Get-AzureEnvironment** per ottenere tutti gli ambienti Azure per l'account.</span><span class="sxs-lookup"><span data-stu-id="cb64e-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="cb64e-122">USA quindi il cmdlet **foreach-Object** per eseguire un comando **Get-AzureEnvironment** con il parametro **Name** in ogni ambiente.</span><span class="sxs-lookup"><span data-stu-id="cb64e-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="cb64e-123">Il valore del parametro **Name** è la proprietà **EnvironmentName** di ogni ambiente.</span><span class="sxs-lookup"><span data-stu-id="cb64e-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="cb64e-124">Senza parametri, **Get-AzureEnvironment** ottiene solo le proprietà selezionate di un ambiente.</span><span class="sxs-lookup"><span data-stu-id="cb64e-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="cb64e-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb64e-125">PARAMETERS</span></span>

### <span data-ttu-id="cb64e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb64e-126">-Name</span></span>
<span data-ttu-id="cb64e-127">Ottiene solo l'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="cb64e-127">Gets only the specified environment.</span></span>
<span data-ttu-id="cb64e-128">Digitare il nome dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="cb64e-128">Type the environment name.</span></span>
<span data-ttu-id="cb64e-129">Il valore del parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cb64e-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="cb64e-130">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="cb64e-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb64e-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="cb64e-131">-Profile</span></span>
<span data-ttu-id="cb64e-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb64e-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cb64e-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cb64e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb64e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb64e-134">CommonParameters</span></span>
<span data-ttu-id="cb64e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb64e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb64e-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb64e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb64e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb64e-137">INPUTS</span></span>

### <span data-ttu-id="cb64e-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cb64e-138">None</span></span>
<span data-ttu-id="cb64e-139">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="cb64e-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="cb64e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb64e-140">OUTPUTS</span></span>

### <span data-ttu-id="cb64e-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="cb64e-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="cb64e-142">Per impostazione predefinita, **Get-AzureEnvironment** restituisce un oggetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cb64e-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="cb64e-143">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb64e-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="cb64e-144">Quando si esegue **Get-AzureEnvironment** con il parametro **Name** , viene restituito un oggetto  **WindowsAzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="cb64e-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="cb64e-145">Note</span><span class="sxs-lookup"><span data-stu-id="cb64e-145">NOTES</span></span>

## <span data-ttu-id="cb64e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb64e-146">RELATED LINKS</span></span>

[<span data-ttu-id="cb64e-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="cb64e-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="cb64e-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb64e-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="cb64e-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cb64e-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="cb64e-150">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cb64e-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="cb64e-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb64e-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="cb64e-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb64e-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


