---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023887"
---
# <span data-ttu-id="d29c3-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d29c3-101">New-AzureDeployment</span></span>

## <span data-ttu-id="d29c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d29c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d29c3-103">Crea una distribuzione da un servizio.</span><span class="sxs-lookup"><span data-stu-id="d29c3-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="d29c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d29c3-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d29c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d29c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d29c3-106">Il cmdlet **New-AzureDeployment** crea una distribuzione di Azure da un servizio che include ruoli Web e ruoli di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d29c3-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="d29c3-107">Questo cmdlet crea una distribuzione basata su un file di pacchetto (con estensione cspkg) e un file di configurazione del servizio (con estensione cscfg).</span><span class="sxs-lookup"><span data-stu-id="d29c3-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="d29c3-108">Specificare un nome univoco all'interno dell'ambiente di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="d29c3-109">Usa il cmdlet **New-AzureVM** per creare una distribuzione basata su macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="d29c3-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="d29c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d29c3-110">EXAMPLES</span></span>

### <span data-ttu-id="d29c3-111">Esempio 1: creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d29c3-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="d29c3-112">Questo comando crea una distribuzione di produzione basata su un pacchetto denominato ContosoPackage. cspkg e una configurazione denominata ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="d29c3-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="d29c3-113">Il comando specifica un'etichetta per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="d29c3-114">Non specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="d29c3-114">It does not specify a name.</span></span>
<span data-ttu-id="d29c3-115">Questo cmdlet crea un GUID come nome.</span><span class="sxs-lookup"><span data-stu-id="d29c3-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="d29c3-116">Esempio 2: creare una distribuzione in base a una configurazione di estensione</span><span class="sxs-lookup"><span data-stu-id="d29c3-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="d29c3-117">Questo comando crea una distribuzione di produzione in base a un pacchetto e a una configurazione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="d29c3-118">Il comando specifica una configurazione di estensione denominata ContosoExtensionConfig. cscfg.</span><span class="sxs-lookup"><span data-stu-id="d29c3-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="d29c3-119">Questo cmdlet crea GUID come nome e etichetta.</span><span class="sxs-lookup"><span data-stu-id="d29c3-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="d29c3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d29c3-120">PARAMETERS</span></span>

### <span data-ttu-id="d29c3-121">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="d29c3-121">-Configuration</span></span>
<span data-ttu-id="d29c3-122">Specifica il percorso completo di un file di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="d29c3-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="d29c3-123">-DoNotStart</span></span>
<span data-ttu-id="d29c3-124">Specifica che il cmdlet non avvia la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="d29c3-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="d29c3-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="d29c3-126">Specifica una matrice di oggetti di configurazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d29c3-127">-InformationAction</span></span>
<span data-ttu-id="d29c3-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d29c3-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d29c3-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d29c3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d29c3-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="d29c3-130">Continue</span></span>
- <span data-ttu-id="d29c3-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="d29c3-131">Ignore</span></span>
- <span data-ttu-id="d29c3-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d29c3-132">Inquire</span></span>
- <span data-ttu-id="d29c3-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d29c3-133">SilentlyContinue</span></span>
- <span data-ttu-id="d29c3-134">Stop</span><span class="sxs-lookup"><span data-stu-id="d29c3-134">Stop</span></span>
- <span data-ttu-id="d29c3-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d29c3-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d29c3-136">-InformationVariable</span></span>
<span data-ttu-id="d29c3-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d29c3-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-138">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="d29c3-138">-Label</span></span>
<span data-ttu-id="d29c3-139">Specifica un nome di etichetta per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="d29c3-140">Se non specifichi un'etichetta, questo cmdlet usa un GUID.</span><span class="sxs-lookup"><span data-stu-id="d29c3-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="d29c3-141">-Name</span></span>
<span data-ttu-id="d29c3-142">Specifica un nome di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-142">Specifies a deployment name.</span></span>
<span data-ttu-id="d29c3-143">Se non specifichi un nome, questo cmdlet usa un GUID.</span><span class="sxs-lookup"><span data-stu-id="d29c3-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-144">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="d29c3-144">-Package</span></span>
<span data-ttu-id="d29c3-145">Specifica il percorso o l'URI di un file con estensione cspkg nell'archiviazione nello stesso abbonamento o progetto.</span><span class="sxs-lookup"><span data-stu-id="d29c3-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="d29c3-146">-Profile</span></span>
<span data-ttu-id="d29c3-147">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29c3-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d29c3-148">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d29c3-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d29c3-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d29c3-149">-ServiceName</span></span>
<span data-ttu-id="d29c3-150">Specifica il nome del servizio Azure per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="d29c3-151">-Slot</span></span>
<span data-ttu-id="d29c3-152">Specifica l'ambiente in cui questo cmdlet crea la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="d29c3-153">I valori validi sono: staging e produzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="d29c3-154">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="d29c3-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c3-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="d29c3-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="d29c3-156">Specifica che i messaggi di avviso sono errori.</span><span class="sxs-lookup"><span data-stu-id="d29c3-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="d29c3-157">Se specifichi questo parametro, un messaggio di avviso causa l'errore della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d29c3-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="d29c3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29c3-158">CommonParameters</span></span>
<span data-ttu-id="d29c3-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29c3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29c3-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29c3-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29c3-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d29c3-161">INPUTS</span></span>

## <span data-ttu-id="d29c3-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d29c3-162">OUTPUTS</span></span>

## <span data-ttu-id="d29c3-163">Note</span><span class="sxs-lookup"><span data-stu-id="d29c3-163">NOTES</span></span>

## <span data-ttu-id="d29c3-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d29c3-164">RELATED LINKS</span></span>

[<span data-ttu-id="d29c3-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d29c3-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="d29c3-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="d29c3-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="d29c3-167">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d29c3-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="d29c3-168">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d29c3-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="d29c3-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d29c3-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="d29c3-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d29c3-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


