---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023908"
---
# <span data-ttu-id="f8ade-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f8ade-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="f8ade-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8ade-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ade-103">Cambia un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ade-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="f8ade-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8ade-104">SYNTAX</span></span>

### <span data-ttu-id="f8ade-105">UpdateSubscriptionByIdParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8ade-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f8ade-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f8ade-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f8ade-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f8ade-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ade-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8ade-108">DESCRIPTION</span></span>
<span data-ttu-id="f8ade-109">Il cmdlet **set-AzureSubscription** stabilisce e modifica le proprietà di un oggetto abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ade-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="f8ade-110">Puoi usare questo cmdlet per lavorare in un abbonamento a Azure che non è l'abbonamento predefinito o per cambiare l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f8ade-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="f8ade-111">Per informazioni sulle sottoscrizioni correnti e predefinite, vedere il cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="f8ade-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="f8ade-112">Questo cmdlet opera su un oggetto abbonamento Azure, non sull'abbonamento Azure effettivo.</span><span class="sxs-lookup"><span data-stu-id="f8ade-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="f8ade-113">Per creare e eseguire il provisioning di un abbonamento a Azure, visitare il [portale di Azure](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="f8ade-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="f8ade-114">Questo cmdlet modifica i dati nel file di dati dell'abbonamento creato quando si usa il cmdlet **Add-AzureAccount** o **Import-AzurePublishSettingsFile** per aggiungere un account di Azure a Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8ade-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="f8ade-115">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ade-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f8ade-116">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f8ade-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="f8ade-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8ade-117">EXAMPLES</span></span>

### <span data-ttu-id="f8ade-118">Esempio 1: cambiare un Subscription1 esistente</span><span class="sxs-lookup"><span data-stu-id="f8ade-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="f8ade-119">Questo esempio modifica il certificato per l'abbonamento denominato ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="f8ade-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="f8ade-120">Esempio 2: modificare l'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="f8ade-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="f8ade-121">Questo comando aggiunge o modifica un endpoint di servizio personalizzato per l'abbonamento a ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="f8ade-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="f8ade-122">Esempio 3: cancellare i valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f8ade-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="f8ade-123">Questo comando imposta i valori delle proprietà certificate e ResourceManagerEndpoint su null ($Null).</span><span class="sxs-lookup"><span data-stu-id="f8ade-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="f8ade-124">In questo modo vengono cancellati i valori di tali proprietà senza modificare altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f8ade-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="f8ade-125">Esempio 4: usare un file di dati alternativo per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f8ade-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="f8ade-126">Questo comando cambia l'account di archiviazione corrente dell'abbonamento a ContosoFinance in ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="f8ade-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="f8ade-127">Il comando usa il parametro **SubscriptionDataFile** per modificare i dati nel file di dati dell'abbonamento C:\Azure\SubscriptionData.xml.</span><span class="sxs-lookup"><span data-stu-id="f8ade-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="f8ade-128">Per impostazione predefinita, **set-AzureSubscription** usa il file di dati di sottoscrizione predefinito nel profilo utente roaming.</span><span class="sxs-lookup"><span data-stu-id="f8ade-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="f8ade-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8ade-129">PARAMETERS</span></span>

### <span data-ttu-id="f8ade-130">-Certificato</span><span class="sxs-lookup"><span data-stu-id="f8ade-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ade-131">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f8ade-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ade-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8ade-132">-CurrentStorageAccountName</span></span>
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

### <span data-ttu-id="f8ade-133">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="f8ade-133">-Environment</span></span>
<span data-ttu-id="f8ade-134">Specifica un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ade-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="f8ade-135">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="f8ade-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f8ade-136">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="f8ade-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f8ade-137">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8ade-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="f8ade-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8ade-138">-PassThru</span></span>
<span data-ttu-id="f8ade-139">Restituisce $True se il comando riesce e $False se non riesce.</span><span class="sxs-lookup"><span data-stu-id="f8ade-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="f8ade-140">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="f8ade-140">By default, this cmdlet does not return any output.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ade-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="f8ade-141">-Profile</span></span>
<span data-ttu-id="f8ade-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8ade-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f8ade-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f8ade-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f8ade-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ade-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f8ade-145">Specifica l'endpoint per i dati di gestione risorse di Azure, inclusi i dati relativi ai gruppi di risorse associati all'account.</span><span class="sxs-lookup"><span data-stu-id="f8ade-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="f8ade-146">Per altre informazioni su Azure Resource Manager, vedere [cmdlet di gestione risorse di Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e uso di [Windows PowerShell con Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="f8ade-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="f8ade-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ade-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="f8ade-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8ade-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ade-149">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="f8ade-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ade-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ade-150">CommonParameters</span></span>
<span data-ttu-id="f8ade-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ade-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ade-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ade-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ade-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8ade-153">INPUTS</span></span>

### <span data-ttu-id="f8ade-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8ade-154">None</span></span>
<span data-ttu-id="f8ade-155">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="f8ade-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f8ade-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8ade-156">OUTPUTS</span></span>

### <span data-ttu-id="f8ade-157">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8ade-157">None or System.Boolean</span></span>
<span data-ttu-id="f8ade-158">Quando si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f8ade-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="f8ade-159">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="f8ade-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="f8ade-160">Note</span><span class="sxs-lookup"><span data-stu-id="f8ade-160">NOTES</span></span>

## <span data-ttu-id="f8ade-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8ade-161">RELATED LINKS</span></span>

[<span data-ttu-id="f8ade-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f8ade-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="f8ade-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f8ade-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="f8ade-164">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f8ade-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="f8ade-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f8ade-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="f8ade-166">Selezionare-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f8ade-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


