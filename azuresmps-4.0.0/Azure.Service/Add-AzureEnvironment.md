---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023688"
---
# <span data-ttu-id="690b3-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="690b3-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="690b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="690b3-102">SYNOPSIS</span></span>
<span data-ttu-id="690b3-103">Crea un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="690b3-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="690b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="690b3-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="690b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="690b3-105">DESCRIPTION</span></span>
<span data-ttu-id="690b3-106">Il cmdlet **Add-AzureEnvironment** crea un nuovo ambiente di account Azure personalizzato e lo salva nel profilo utente mobile.</span><span class="sxs-lookup"><span data-stu-id="690b3-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="690b3-107">Il cmdlet restituisce un oggetto che rappresenta il nuovo ambiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="690b3-108">Al termine del comando, è possibile usare l'ambiente in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="690b3-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="690b3-109">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="690b3-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="690b3-110">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="690b3-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="690b3-111">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="690b3-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="690b3-112">Solo il parametro **Name** di questo cmdlet è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="690b3-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="690b3-113">Se si omette un parametro, il relativo valore è null ($Null) e il servizio che usa tale endpoint potrebbe non funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="690b3-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="690b3-114">Per aggiungere o modificare il valore di una proprietà dell'ambiente, usare il cmdlet **set-AzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="690b3-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="690b3-115">Nota: la modifica dell'ambiente può causare un errore dell'account.</span><span class="sxs-lookup"><span data-stu-id="690b3-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="690b3-116">In genere, gli ambienti vengono aggiunti solo per i test o la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="690b3-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="690b3-117">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="690b3-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="690b3-118">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="690b3-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="690b3-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="690b3-119">EXAMPLES</span></span>

### <span data-ttu-id="690b3-120">Esempio 1: aggiungere un ambiente Azure</span><span class="sxs-lookup"><span data-stu-id="690b3-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="690b3-121">Questo comando crea l'ambiente ContosoEnv Azure.</span><span class="sxs-lookup"><span data-stu-id="690b3-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="690b3-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="690b3-122">PARAMETERS</span></span>

### <span data-ttu-id="690b3-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="690b3-124">Specifica l'endpoint per l'autenticazione di Azure Active Directory nel nuovo ambiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="690b3-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="690b3-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="690b3-126">Specifica l'ID risorsa di un'API di gestione il cui accesso è gestito da Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="690b3-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="690b3-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="690b3-127">-AdTenant</span></span>
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

### <span data-ttu-id="690b3-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="690b3-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="690b3-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="690b3-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="690b3-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="690b3-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="690b3-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-131">-GalleryEndpoint</span></span>
<span data-ttu-id="690b3-132">Specifica l'endpoint per la raccolta di gestione risorse di Azure, in cui sono archiviati i modelli della raccolta di gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="690b3-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="690b3-133">Per altre informazioni sui gruppi di risorse Azure e sui modelli di raccolta, vedere l'argomento della Guida per Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="690b3-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="690b3-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="690b3-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="690b3-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="690b3-136">Specifica l'URL del portale di gestione di Azure nel nuovo ambiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="690b3-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="690b3-137">-Name</span></span>
<span data-ttu-id="690b3-138">Specifica un nome per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="690b3-139">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="690b3-139">This parameter is required.</span></span>
<span data-ttu-id="690b3-140">Non usare i nomi degli ambienti predefiniti, AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="690b3-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="690b3-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="690b3-141">-Profile</span></span>
<span data-ttu-id="690b3-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690b3-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="690b3-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="690b3-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="690b3-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="690b3-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="690b3-145">Specifica l'URL dei file di impostazioni di pubblicazione per l'account.</span><span class="sxs-lookup"><span data-stu-id="690b3-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="690b3-146">Un file di impostazioni di pubblicazione di Azure è un file XML che contiene informazioni sul proprio account e un certificato di gestione che consente a Windows PowerShell di accedere all'account di Azure per proprio conto.</span><span class="sxs-lookup"><span data-stu-id="690b3-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="690b3-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="690b3-148">Specifica l'endpoint per i dati di gestione risorse di Azure, inclusi i dati relativi ai gruppi di risorse associati all'account.</span><span class="sxs-lookup"><span data-stu-id="690b3-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="690b3-149">Per altre informazioni su Azure Resource Manager, vedere [cmdlet di gestione risorse di Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e uso di [Windows PowerShell con Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="690b3-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="690b3-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-150">-ServiceEndpoint</span></span>
<span data-ttu-id="690b3-151">Specifica l'URL dell'endpoint di Azure Service.</span><span class="sxs-lookup"><span data-stu-id="690b3-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="690b3-152">L'endpoint di Azure Service determina se l'applicazione è gestita dalla piattaforma Azure globale, Azure gestita da 21Vianet in Cina o da un'installazione privata di Azure.</span><span class="sxs-lookup"><span data-stu-id="690b3-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="690b3-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="690b3-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="690b3-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="690b3-154">-StorageEndpoint</span></span>
<span data-ttu-id="690b3-155">Specifica l'endpoint predefinito dei servizi di archiviazione nel nuovo ambiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="690b3-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="690b3-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="690b3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690b3-157">CommonParameters</span></span>
<span data-ttu-id="690b3-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690b3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690b3-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690b3-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690b3-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="690b3-160">INPUTS</span></span>

### <span data-ttu-id="690b3-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="690b3-161">None</span></span>
<span data-ttu-id="690b3-162">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="690b3-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="690b3-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="690b3-163">OUTPUTS</span></span>

### <span data-ttu-id="690b3-164">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="690b3-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="690b3-165">Note</span><span class="sxs-lookup"><span data-stu-id="690b3-165">NOTES</span></span>

## <span data-ttu-id="690b3-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="690b3-166">RELATED LINKS</span></span>

[<span data-ttu-id="690b3-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="690b3-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="690b3-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="690b3-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="690b3-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="690b3-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


