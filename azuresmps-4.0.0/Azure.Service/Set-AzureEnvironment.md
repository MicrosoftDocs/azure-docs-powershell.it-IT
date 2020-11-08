---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023925"
---
# <span data-ttu-id="e9a40-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9a40-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="e9a40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9a40-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a40-103">Modifica le proprietà di un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a40-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="e9a40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9a40-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9a40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9a40-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a40-106">Il cmdlet **set-AzureEnvironment** modifica le proprietà di un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a40-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="e9a40-107">Restituisce un oggetto che rappresenta l'ambiente con i nuovi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9a40-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="e9a40-108">Usa il parametro **Name** per identificare l'ambiente e gli altri parametri per modificare i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9a40-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="e9a40-109">Non è possibile usare **set-AzureEnvironment** per modificare il nome di un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a40-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="e9a40-110">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="e9a40-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="e9a40-111">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="e9a40-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="e9a40-112">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e9a40-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="e9a40-113">Nota: non modificare le proprietà degli ambienti AzureCloud o AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e9a40-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="e9a40-114">Questo cmdlet consente di modificare i valori degli ambienti privati creati.</span><span class="sxs-lookup"><span data-stu-id="e9a40-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="e9a40-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9a40-115">EXAMPLES</span></span>

### <span data-ttu-id="e9a40-116">Esempio 1: modificare le proprietà dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="e9a40-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="e9a40-117">Questo comando modifica i valori delle proprietà **PublishSettingsFileUrl** e **StorageEndpoint** dell'ambiente ContosoEnv.</span><span class="sxs-lookup"><span data-stu-id="e9a40-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="e9a40-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9a40-118">PARAMETERS</span></span>

### <span data-ttu-id="e9a40-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="e9a40-120">Modifica l'endpoint per l'autenticazione di Azure Active Directory con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e9a40-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="e9a40-122">Specifica l'ID risorsa di un'API di gestione il cui accesso è gestito da Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9a40-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="e9a40-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="e9a40-123">-AdTenant</span></span>
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

### <span data-ttu-id="e9a40-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e9a40-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="e9a40-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e9a40-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="e9a40-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e9a40-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-127">-GalleryEndpoint</span></span>
<span data-ttu-id="e9a40-128">Modifica l'endpoint per la raccolta di gestione risorse di Azure nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="e9a40-129">L'endpoint della raccolta è la posizione per i modelli della raccolta di gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9a40-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="e9a40-130">Per altre informazioni sui gruppi di risorse Azure e sui modelli di raccolta, vedere l'argomento della Guida per [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="e9a40-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="e9a40-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="e9a40-133">Modifica l'URL del portale di gestione di Azure nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="e9a40-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9a40-134">-Name</span></span>
<span data-ttu-id="e9a40-135">Identifica l'ambiente che viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="e9a40-136">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9a40-136">This parameter is required.</span></span>
<span data-ttu-id="e9a40-137">Il valore del parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e9a40-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="e9a40-138">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="e9a40-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9a40-139">-Profile</span></span>
<span data-ttu-id="e9a40-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a40-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e9a40-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e9a40-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9a40-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="e9a40-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="e9a40-143">Modifica l'URL per i file delle impostazioni di pubblicazione nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="e9a40-144">Un file di impostazioni di pubblicazione di Azure è un file XML che contiene informazioni sul proprio account e un certificato di gestione che consente a Windows PowerShell di accedere all'account di Azure per proprio conto.</span><span class="sxs-lookup"><span data-stu-id="e9a40-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="e9a40-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="e9a40-146">Modifica l'endpoint per i dati di gestione risorse di Azure, inclusi i dati relativi ai gruppi di risorse associati all'account.</span><span class="sxs-lookup"><span data-stu-id="e9a40-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="e9a40-147">Per altre informazioni su Azure Resource Manager, vedere [cmdlet di gestione risorse di Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e uso di [Windows PowerShell con Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="e9a40-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-148">-ServiceEndpoint</span></span>
<span data-ttu-id="e9a40-149">Modifica l'URL dell'endpoint di Azure Service nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="e9a40-150">L'endpoint di Azure Service determina se l'applicazione è gestita dalla piattaforma Azure globale, Azure gestita da 21Vianet in Cina o da un'installazione privata di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a40-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e9a40-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="e9a40-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9a40-152">-StorageEndpoint</span></span>
<span data-ttu-id="e9a40-153">Modifica l'endpoint predefinito dei servizi di archiviazione nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="e9a40-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a40-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e9a40-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="e9a40-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a40-155">CommonParameters</span></span>
<span data-ttu-id="e9a40-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a40-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a40-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a40-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a40-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9a40-158">INPUTS</span></span>

### <span data-ttu-id="e9a40-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9a40-159">None</span></span>
<span data-ttu-id="e9a40-160">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="e9a40-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e9a40-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9a40-161">OUTPUTS</span></span>

### <span data-ttu-id="e9a40-162">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9a40-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="e9a40-163">Note</span><span class="sxs-lookup"><span data-stu-id="e9a40-163">NOTES</span></span>

## <span data-ttu-id="e9a40-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9a40-164">RELATED LINKS</span></span>

[<span data-ttu-id="e9a40-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9a40-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="e9a40-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9a40-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="e9a40-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9a40-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


