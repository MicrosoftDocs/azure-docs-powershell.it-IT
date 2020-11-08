---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029723"
---
# <span data-ttu-id="aaac8-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aaac8-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="aaac8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaac8-102">SYNOPSIS</span></span>
<span data-ttu-id="aaac8-103">Importa un file di impostazioni di pubblicazione che consente di gestire gli account di Azure in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aaac8-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="aaac8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaac8-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aaac8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaac8-105">DESCRIPTION</span></span>
<span data-ttu-id="aaac8-106">Il cmdlet **Import-AzurePublishSettingsFile** importa un file di impostazioni di pubblicazione (\*. publishsettings) che contiene informazioni sugli account di Azure e salva un file di dati di sottoscrizione nel computer.</span><span class="sxs-lookup"><span data-stu-id="aaac8-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="aaac8-107">Al termine del cmdlet, è possibile gestire gli account di Azure in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aaac8-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="aaac8-108">Prima di eseguire **Import-AzurePublishSettingsFile** , Esegui **Get-AzurePublishSettingsFile** , che Scarica e salva il file delle impostazioni di pubblicazione in modo da poterlo importare.</span><span class="sxs-lookup"><span data-stu-id="aaac8-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="aaac8-109">Per rendere l'account di Azure disponibile per Windows PowerShell, è possibile usare un file di impostazioni di pubblicazione o il cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="aaac8-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="aaac8-110">I file di impostazioni di pubblicazione consentono di preparare la sessione in anticipo, in modo da poter eseguire script e processi in background incustoditi.</span><span class="sxs-lookup"><span data-stu-id="aaac8-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="aaac8-111">Tuttavia, non tutti i servizi supportano i file delle impostazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="aaac8-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="aaac8-112">Ad esempio, il modulo **AzureResourceManager** non supporta i file delle impostazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="aaac8-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="aaac8-113">**Nota sulla sicurezza:** I file delle impostazioni di pubblicazione contengono un certificato di gestione codificato, ma non crittografato.</span><span class="sxs-lookup"><span data-stu-id="aaac8-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="aaac8-114">Se gli utenti malintenzionati accedono al file delle impostazioni di pubblicazione, potrebbero essere in grado di modificare, creare ed eliminare i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="aaac8-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="aaac8-115">Come procedura consigliata per la sicurezza, salvare il file in un percorso nella cartella download o documenti e quindi eliminarlo dopo avere usato il cmdlet **Import-AzurePublishSettingsFile** per importare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="aaac8-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="aaac8-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaac8-116">EXAMPLES</span></span>

### <span data-ttu-id="aaac8-117">Esempio 1: importare un file</span><span class="sxs-lookup"><span data-stu-id="aaac8-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="aaac8-118">Questo comando importa il file "C:\Temp\MyAccount.publishsettings".</span><span class="sxs-lookup"><span data-stu-id="aaac8-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="aaac8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaac8-119">PARAMETERS</span></span>

### <span data-ttu-id="aaac8-120">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="aaac8-120">-Environment</span></span>
<span data-ttu-id="aaac8-121">Specifica un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="aaac8-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="aaac8-122">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="aaac8-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="aaac8-123">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="aaac8-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="aaac8-124">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aaac8-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaac8-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="aaac8-125">-Profile</span></span>
<span data-ttu-id="aaac8-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaac8-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aaac8-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="aaac8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aaac8-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aaac8-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="aaac8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaac8-129">CommonParameters</span></span>
<span data-ttu-id="aaac8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaac8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaac8-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaac8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaac8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaac8-132">INPUTS</span></span>

### <span data-ttu-id="aaac8-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaac8-133">None</span></span>
<span data-ttu-id="aaac8-134">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="aaac8-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="aaac8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaac8-135">OUTPUTS</span></span>

### <span data-ttu-id="aaac8-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaac8-136">None</span></span>
<span data-ttu-id="aaac8-137">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="aaac8-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aaac8-138">Note</span><span class="sxs-lookup"><span data-stu-id="aaac8-138">NOTES</span></span>
* <span data-ttu-id="aaac8-139">Un file di impostazioni di pubblicazione è un file XML con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="aaac8-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="aaac8-140">Il file contiene un certificato codificato che fornisce le credenziali di gestione per gli abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="aaac8-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="aaac8-141">Dopo aver importato il file, eliminarlo per evitare rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aaac8-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="aaac8-142">Un "file di dati di sottoscrizione" è un file XML che può essere salvato nel computer in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="aaac8-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="aaac8-143">Per impostazione predefinita, viene salvato nel profilo utente roaming ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="aaac8-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="aaac8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaac8-144">RELATED LINKS</span></span>

[<span data-ttu-id="aaac8-145">Come installare e configurare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aaac8-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="aaac8-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="aaac8-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="aaac8-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aaac8-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


