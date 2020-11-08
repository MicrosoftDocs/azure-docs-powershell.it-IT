---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023591"
---
# <span data-ttu-id="874d6-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="874d6-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="874d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="874d6-102">SYNOPSIS</span></span>
<span data-ttu-id="874d6-103">Scarica il file delle impostazioni di pubblicazione per un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="874d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="874d6-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="874d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="874d6-105">DESCRIPTION</span></span>
<span data-ttu-id="874d6-106">Il cmdlet **Get-AzurePublishSettingsFile** Scarica un file di impostazioni di pubblicazione per un abbonamento nell'account.</span><span class="sxs-lookup"><span data-stu-id="874d6-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="874d6-107">Al termine del comando, è possibile usare il cmdlet **Import-PublishSettingsFile** per rendere le impostazioni del file disponibili per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="874d6-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="874d6-108">Per rendere l'account di Azure disponibile per Windows PowerShell, è possibile usare un file di impostazioni di pubblicazione o il cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="874d6-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="874d6-109">I file di impostazioni di pubblicazione consentono di preparare la sessione in anticipo, in modo da poter eseguire script e processi in background incustoditi.</span><span class="sxs-lookup"><span data-stu-id="874d6-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="874d6-110">Tuttavia, non tutti i servizi supportano i file delle impostazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="874d6-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="874d6-111">Ad esempio, il modulo **AzureResourceManager** non supporta i file delle impostazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="874d6-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="874d6-112">Quando si esegue **Get-AzurePublishSettingsFile** , viene aperto il browser predefinito e viene chiesto di accedere all'account di Azure, selezionare un abbonamento e selezionare un percorso di file System per il file delle impostazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="874d6-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="874d6-113">Quindi, Scarica il file delle impostazioni di pubblicazione per l'abbonamento nel file selezionato.</span><span class="sxs-lookup"><span data-stu-id="874d6-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="874d6-114">Un file di impostazioni di pubblicazione è un file XML con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="874d6-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="874d6-115">Il file contiene un certificato codificato che fornisce le credenziali di gestione per gli abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="874d6-116">**Nota sulla sicurezza:** I file delle impostazioni di pubblicazione contengono le credenziali usate per amministrare gli abbonamenti e i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="874d6-117">Se gli utenti malintenzionati accedono al file delle impostazioni di pubblicazione, possono modificare, creare ed eliminare i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="874d6-118">Come procedura consigliata per la sicurezza, salvare il file in un percorso nella cartella download o documenti e quindi eliminarlo dopo avere usato il cmdlet **Import-AzurePublishSettingsFile** per importare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="874d6-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="874d6-119">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="874d6-120">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="874d6-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="874d6-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="874d6-121">EXAMPLES</span></span>

### <span data-ttu-id="874d6-122">Esempio 1: scaricare un file di impostazioni di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="874d6-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="874d6-123">Questo comando apre il browser predefinito, si connette all'account di Windows Azure e quindi Scarica il file con estensione publishsettings per l'account.</span><span class="sxs-lookup"><span data-stu-id="874d6-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="874d6-124">Esempio 2: specificare un Realm</span><span class="sxs-lookup"><span data-stu-id="874d6-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="874d6-125">Questo comando Scarica il file delle impostazioni di pubblicazione per un account nel dominio contoso.com.</span><span class="sxs-lookup"><span data-stu-id="874d6-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="874d6-126">Usare un comando con il parametro **Realm** quando si accede a Azure con un account aziendale, invece di un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="874d6-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="874d6-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="874d6-127">PARAMETERS</span></span>

### <span data-ttu-id="874d6-128">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="874d6-128">-Environment</span></span>
<span data-ttu-id="874d6-129">Specifica un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="874d6-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="874d6-130">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="874d6-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="874d6-131">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="874d6-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="874d6-132">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="874d6-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="874d6-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="874d6-133">-PassThru</span></span>
<span data-ttu-id="874d6-134">Restituisce $True se il comando riesce e $False se non riesce.</span><span class="sxs-lookup"><span data-stu-id="874d6-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="874d6-135">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="874d6-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="874d6-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="874d6-136">-Profile</span></span>
<span data-ttu-id="874d6-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="874d6-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="874d6-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="874d6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="874d6-139">-Realm</span><span class="sxs-lookup"><span data-stu-id="874d6-139">-Realm</span></span>
<span data-ttu-id="874d6-140">Specifica l'organizzazione in un ID organizzativo.</span><span class="sxs-lookup"><span data-stu-id="874d6-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="874d6-141">Ad esempio, se si accede a Azure As admin@contoso.com , il valore del parametro **Realm** è contoso.com.</span><span class="sxs-lookup"><span data-stu-id="874d6-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="874d6-142">Usa questo parametro quando usi un ID organizzazione per accedere a Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="874d6-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="874d6-143">Questo parametro non è necessario quando si usa un account Microsoft, ad esempio un account di outlook.com o live.com.</span><span class="sxs-lookup"><span data-stu-id="874d6-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="874d6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874d6-144">CommonParameters</span></span>
<span data-ttu-id="874d6-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="874d6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874d6-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874d6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874d6-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="874d6-147">INPUTS</span></span>

### <span data-ttu-id="874d6-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="874d6-148">None</span></span>
<span data-ttu-id="874d6-149">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="874d6-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="874d6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="874d6-150">OUTPUTS</span></span>

### <span data-ttu-id="874d6-151">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="874d6-151">None or System.Boolean</span></span>
<span data-ttu-id="874d6-152">Quando si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="874d6-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="874d6-153">In caso contrario, questo cmdlet non restituisce alcun output</span><span class="sxs-lookup"><span data-stu-id="874d6-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="874d6-154">Note</span><span class="sxs-lookup"><span data-stu-id="874d6-154">NOTES</span></span>

## <span data-ttu-id="874d6-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="874d6-155">RELATED LINKS</span></span>

[<span data-ttu-id="874d6-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="874d6-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="874d6-157">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="874d6-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


