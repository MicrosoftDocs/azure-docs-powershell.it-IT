---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023841"
---
# <span data-ttu-id="496a0-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="496a0-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="496a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="496a0-102">SYNOPSIS</span></span>
<span data-ttu-id="496a0-103">Pubblicare il servizio corrente in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="496a0-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="496a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="496a0-104">SYNTAX</span></span>

### <span data-ttu-id="496a0-105">PublishFromServiceDefinition (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="496a0-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="496a0-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="496a0-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="496a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="496a0-107">DESCRIPTION</span></span>
<span data-ttu-id="496a0-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="496a0-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="496a0-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="496a0-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="496a0-110">Il cmdlet **Publish-AzureServiceProject** pubblica il servizio corrente nel cloud.</span><span class="sxs-lookup"><span data-stu-id="496a0-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="496a0-111">È possibile specificare la configurazione di pubblicazione, ad esempio **Subscription** , **StorageAccountName** , **location** , **slot** , nella riga di comando o in impostazioni locali tramite il cmdlet **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="496a0-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="496a0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="496a0-112">EXAMPLES</span></span>

### <span data-ttu-id="496a0-113">Esempio 1: pubblicare un progetto di servizio con i valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="496a0-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="496a0-114">Questo esempio pubblica il servizio corrente, usando le impostazioni correnti del servizio e il profilo di pubblicazione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="496a0-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="496a0-115">Esempio 2: creare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="496a0-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="496a0-116">Questo esempio crea un file del pacchetto di distribuzione (con estensione cspkg) nella directory del servizio e non viene pubblicato in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="496a0-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="496a0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="496a0-117">PARAMETERS</span></span>

### <span data-ttu-id="496a0-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="496a0-118">-AffinityGroup</span></span>
<span data-ttu-id="496a0-119">Specifica il gruppo di affinità che si desidera venga usato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-120">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="496a0-120">-Configuration</span></span>
<span data-ttu-id="496a0-121">Specifica il file di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="496a0-122">Se specifichi questo parametro, specifica il parametro del *pacchetto* .</span><span class="sxs-lookup"><span data-stu-id="496a0-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="496a0-123">-DeploymentName</span></span>
<span data-ttu-id="496a0-124">Specifica il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="496a0-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="496a0-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-126">-Avvio</span><span class="sxs-lookup"><span data-stu-id="496a0-126">-Launch</span></span>
<span data-ttu-id="496a0-127">Apre una finestra del browser in modo da poter visualizzare l'applicazione dopo la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="496a0-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="496a0-128">-Location</span></span>
<span data-ttu-id="496a0-129">Area geografica in cui verrà ospitata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="496a0-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="496a0-130">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="496a0-130">Possible values are:</span></span> 
  
- <span data-ttu-id="496a0-131">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="496a0-131">Anywhere Asia</span></span>
- <span data-ttu-id="496a0-132">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="496a0-132">Anywhere Europe</span></span>
- <span data-ttu-id="496a0-133">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="496a0-133">Anywhere US</span></span>
- <span data-ttu-id="496a0-134">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="496a0-134">East Asia</span></span>
- <span data-ttu-id="496a0-135">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="496a0-135">East US</span></span>
- <span data-ttu-id="496a0-136">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="496a0-136">North Central US</span></span>
- <span data-ttu-id="496a0-137">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="496a0-137">North Europe</span></span>
- <span data-ttu-id="496a0-138">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="496a0-138">South Central US</span></span>
- <span data-ttu-id="496a0-139">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="496a0-139">Southeast Asia</span></span>
- <span data-ttu-id="496a0-140">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="496a0-140">West Europe</span></span>
- <span data-ttu-id="496a0-141">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="496a0-141">West US</span></span>
 
<span data-ttu-id="496a0-142">Se non è specificata alcuna posizione, verrà usata la posizione specificata nell'ultima chiamata a **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="496a0-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="496a0-143">Se non è stata mai specificata alcuna posizione, la posizione verrà selezionata in modo casuale dalle posizioni "North Central US" e "South Central US".</span><span class="sxs-lookup"><span data-stu-id="496a0-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-144">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="496a0-144">-Package</span></span>
<span data-ttu-id="496a0-145">Specifica il file del pacchetto da distribuire.</span><span class="sxs-lookup"><span data-stu-id="496a0-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="496a0-146">Specifica un file locale con estensione cspkg o un URI di un BLOB contenente il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="496a0-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="496a0-147">Se specifichi questo parametro, non specificare il parametro *ServiceName* .</span><span class="sxs-lookup"><span data-stu-id="496a0-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="496a0-148">-Profile</span></span>
<span data-ttu-id="496a0-149">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496a0-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="496a0-150">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="496a0-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="496a0-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="496a0-151">-ServiceName</span></span>
<span data-ttu-id="496a0-152">Specifica il nome da usare per il servizio durante la pubblicazione in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="496a0-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="496a0-153">Il nome determina parte dell'etichetta nel sottodominio cloudapp.net usato per indirizzare il servizio quando è ospitato in Windows Azure, ovvero **Name**. cloudapp.NET.</span><span class="sxs-lookup"><span data-stu-id="496a0-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="496a0-154">Qualsiasi nome specificato durante la pubblicazione del servizio sostituisce il nome assegnato al momento della creazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="496a0-155">Vedere il cmdlet **New-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="496a0-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="496a0-156">-Slot</span></span>
<span data-ttu-id="496a0-157">Slot di distribuzione da usare per questo servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="496a0-158">I valori possibili sono "Staging" e "Production".</span><span class="sxs-lookup"><span data-stu-id="496a0-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="496a0-159">Se non viene specificato alcuno slot, viene usato lo slot specificato nell'ultima chiamata a Set-AzureDeploymentSlot.</span><span class="sxs-lookup"><span data-stu-id="496a0-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="496a0-160">Se non è mai stato specificato alcuno slot, viene usato lo slot di produzione.</span><span class="sxs-lookup"><span data-stu-id="496a0-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="496a0-161">-StorageAccountName</span></span>
<span data-ttu-id="496a0-162">Specifica il nome dell'account di archiviazione di Windows Azure da usare durante la pubblicazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="496a0-163">Questo valore non viene usato finché non viene pubblicato il servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="496a0-164">Quando questo parametro non viene specificato, il valore viene ottenuto dall'ultimo comando **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="496a0-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="496a0-165">Se non è mai stato specificato alcun account di archiviazione, verrà usato un account di archiviazione corrispondente al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="496a0-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="496a0-166">Se non esiste un account di archiviazione di questo tipo, il cmdlet tenta di crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="496a0-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="496a0-167">Tuttavia, il tentativo potrebbe non riuscire se un account di archiviazione corrispondente al nome del servizio esiste in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="496a0-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496a0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496a0-168">CommonParameters</span></span>
<span data-ttu-id="496a0-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496a0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496a0-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496a0-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496a0-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="496a0-171">INPUTS</span></span>

## <span data-ttu-id="496a0-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="496a0-172">OUTPUTS</span></span>

## <span data-ttu-id="496a0-173">Note</span><span class="sxs-lookup"><span data-stu-id="496a0-173">NOTES</span></span>

## <span data-ttu-id="496a0-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="496a0-174">RELATED LINKS</span></span>

[<span data-ttu-id="496a0-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="496a0-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="496a0-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="496a0-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


