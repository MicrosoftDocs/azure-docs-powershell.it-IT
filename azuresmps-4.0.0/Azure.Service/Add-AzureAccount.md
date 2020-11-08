---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029858"
---
# <span data-ttu-id="6ab67-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6ab67-101">Add-AzureAccount</span></span>

## <span data-ttu-id="6ab67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ab67-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab67-103">Aggiunge l'account di Azure a Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="6ab67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ab67-104">SYNTAX</span></span>

### <span data-ttu-id="6ab67-105">Utente (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ab67-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ab67-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ab67-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ab67-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ab67-107">DESCRIPTION</span></span>
<span data-ttu-id="6ab67-108">Il cmdlet **Add-AzureAccount** rende disponibile l'account Azure e le relative sottoscrizioni in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="6ab67-109">È come accedere all'account di Azure in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="6ab67-110">Per disconnettersi dall'account, usare il cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="6ab67-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="6ab67-111">**Add-AzureAccount** Scarica le informazioni relative all'account di Azure e la Salva in un file di dati di sottoscrizione nel profilo utente mobile.</span><span class="sxs-lookup"><span data-stu-id="6ab67-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="6ab67-112">Viene inoltre ottenuto un token di accesso che consente a Windows PowerShell di accedere all'account di Azure per conto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6ab67-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="6ab67-113">Al termine del comando, puoi gestire l'account di Azure in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="6ab67-114">Esistono due modi diversi per rendere l'account di Azure disponibile per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="6ab67-115">Puoi usare il cmdlet **Add-AzureAccount** , che usa i token di accesso per l'autenticazione di Azure Active Directory (Azure ad) o **Import-AzurePublishSettingsFile** , che usa un certificato di gestione.</span><span class="sxs-lookup"><span data-stu-id="6ab67-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="6ab67-116">Per informazioni su quale metodo usare, vedere [procedura: connettersi all'abbonamento](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="6ab67-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="6ab67-117">Quando si esegue **Add-AzureAccount** , viene visualizzata una finestra interattiva in cui viene richiesto di accedere all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab67-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="6ab67-118">Questo accesso è valido fino alla scadenza del token di Access.</span><span class="sxs-lookup"><span data-stu-id="6ab67-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="6ab67-119">Quando scade, i cmdlet che richiedono l'accesso all'account ti chiedono di eseguire di nuovo l'esecuzione di **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="6ab67-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="6ab67-120">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab67-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6ab67-121">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6ab67-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="6ab67-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ab67-122">EXAMPLES</span></span>

### <span data-ttu-id="6ab67-123">Esempio 1: aggiungere un account</span><span class="sxs-lookup"><span data-stu-id="6ab67-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="6ab67-124">Questo comando aggiunge un account di Azure a Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ab67-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="6ab67-125">Quando si esegue il comando, viene visualizzata una finestra per richiedere il nome utente e la password dell'account.</span><span class="sxs-lookup"><span data-stu-id="6ab67-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="6ab67-126">Esempio 2: usare un file di dati alternativo per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="6ab67-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="6ab67-127">Questo comando usa il parametro **SubscriptionDataFile** per indirizzare **Add-AzureAccount** per archiviare i dati dell'account nel file C:\Testing\SDF.xml, invece che nel file predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ab67-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="6ab67-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ab67-128">PARAMETERS</span></span>

### <span data-ttu-id="6ab67-129">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="6ab67-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab67-130">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="6ab67-130">-Environment</span></span>
<span data-ttu-id="6ab67-131">Specifica un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab67-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="6ab67-132">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="6ab67-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="6ab67-133">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="6ab67-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="6ab67-134">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6ab67-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="6ab67-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ab67-135">-Profile</span></span>
<span data-ttu-id="6ab67-136">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab67-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6ab67-137">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6ab67-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ab67-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ab67-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab67-139">-Tenant</span><span class="sxs-lookup"><span data-stu-id="6ab67-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab67-140">CommonParameters</span></span>
<span data-ttu-id="6ab67-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab67-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab67-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab67-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ab67-143">INPUTS</span></span>

### <span data-ttu-id="6ab67-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6ab67-144">None</span></span>
<span data-ttu-id="6ab67-145">Non è possibile reindirizzare l'input a questo cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ab67-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="6ab67-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ab67-146">OUTPUTS</span></span>

### <span data-ttu-id="6ab67-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6ab67-147">None</span></span>
<span data-ttu-id="6ab67-148">Questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ab67-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="6ab67-149">Note</span><span class="sxs-lookup"><span data-stu-id="6ab67-149">NOTES</span></span>
* <span data-ttu-id="6ab67-150">**Add-AzureAccount** (e il metodo di autenticazione di Azure ad) hanno la precedenza su **Import-AzurePublishSettings** (e il metodo del certificato di gestione).</span><span class="sxs-lookup"><span data-stu-id="6ab67-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="6ab67-151">Se si usa **Add-AzureAccount** anche una volta nel proprio account, viene usato il metodo di autenticazione di Azure ad e il certificato di gestione viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6ab67-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="6ab67-152">Per rimuovere il token Azure AD e ripristinare il metodo di gestione del certificato, usare il cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="6ab67-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="6ab67-153">Per altre informazioni, digitare: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="6ab67-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="6ab67-154">Errore "le credenziali sono scadute.</span><span class="sxs-lookup"><span data-stu-id="6ab67-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="6ab67-155">Usare Add-AzureAccount per accedere di nuovo.</span><span class="sxs-lookup"><span data-stu-id="6ab67-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="6ab67-156">indica che il token di accesso è scaduto e che Windows PowerShell non può accedere all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab67-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="6ab67-157">Per ripristinare l'accesso al proprio account, eseguire di nuovo **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="6ab67-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="6ab67-158">I cmdlet di account e abbonamento di Azure PowerShell ottengono i loro dati dal file di dati dell'abbonamento, non dall'account di Azure Live.</span><span class="sxs-lookup"><span data-stu-id="6ab67-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="6ab67-159">Se si modifica l'account o gli abbonamenti all'esterno di Windows PowerShell, ad esempio tramite il portale di gestione di Azure, eseguire di nuovo **Add-AzureAccount** per aggiornare il file di dati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6ab67-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="6ab67-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ab67-160">RELATED LINKS</span></span>

[<span data-ttu-id="6ab67-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6ab67-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="6ab67-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6ab67-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="6ab67-163">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6ab67-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="6ab67-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6ab67-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="6ab67-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6ab67-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


