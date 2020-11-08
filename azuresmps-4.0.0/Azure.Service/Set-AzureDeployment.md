---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029526"
---
# <span data-ttu-id="a3486-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a3486-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="a3486-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3486-102">SYNOPSIS</span></span>
<span data-ttu-id="a3486-103">Modifica lo stato, le impostazioni di configurazione o la modalità di aggiornamento di una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="a3486-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3486-104">SYNTAX</span></span>

### <span data-ttu-id="a3486-105">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a3486-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3486-106">Config</span><span class="sxs-lookup"><span data-stu-id="a3486-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3486-107">Stato</span><span class="sxs-lookup"><span data-stu-id="a3486-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3486-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3486-108">DESCRIPTION</span></span>
<span data-ttu-id="a3486-109">Il cmdlet **set-AzureDeployment** modifica lo stato, le impostazioni di configurazione o la modalità di aggiornamento di una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3486-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="a3486-110">È possibile modificare lo stato della distribuzione su in corso o sospeso.</span><span class="sxs-lookup"><span data-stu-id="a3486-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="a3486-111">È possibile modificare il file con estensione cscfg per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="a3486-112">Puoi impostare la modalità di aggiornamento e i file di configurazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a3486-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="a3486-113">Usa il cmdlet **set-AzureWalkUpgradeDomain** per avviare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a3486-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="a3486-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3486-114">EXAMPLES</span></span>

### <span data-ttu-id="a3486-115">Esempio 1: modificare lo stato di una distribuzione</span><span class="sxs-lookup"><span data-stu-id="a3486-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="a3486-116">Questo comando imposta lo stato della distribuzione per il servizio denominato ContosoService nell'ambiente di produzione per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a3486-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="a3486-117">Esempio 2: assegnare un file di configurazione diverso a una distribuzione</span><span class="sxs-lookup"><span data-stu-id="a3486-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="a3486-118">Questo comando assegna un file di configurazione diverso per la distribuzione per il servizio denominato ContosoService nell'ambiente di staging.</span><span class="sxs-lookup"><span data-stu-id="a3486-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="a3486-119">Esempio 3: impostare la modalità di aggiornamento su auto</span><span class="sxs-lookup"><span data-stu-id="a3486-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="a3486-120">Questo comando imposta la modalità di aggiornamento su auto e specifica un pacchetto di aggiornamento e un nuovo file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a3486-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="a3486-121">Esempio 4: installare la configurazione dell'estensione in un servizio</span><span class="sxs-lookup"><span data-stu-id="a3486-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="a3486-122">Questo comando consente di installare la configurazione dell'estensione nel servizio cloud specificato e di applicarla ai ruoli.</span><span class="sxs-lookup"><span data-stu-id="a3486-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="a3486-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3486-123">PARAMETERS</span></span>

### <span data-ttu-id="a3486-124">-Config</span><span class="sxs-lookup"><span data-stu-id="a3486-124">-Config</span></span>
<span data-ttu-id="a3486-125">Specifica che questo cmdlet modifica la configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-126">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="a3486-126">-Configuration</span></span>
<span data-ttu-id="a3486-127">Specifica il percorso completo di un file di configurazione cscfg.</span><span class="sxs-lookup"><span data-stu-id="a3486-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="a3486-128">È possibile specificare un file di configurazione per un aggiornamento o una modifica della configurazione.</span><span class="sxs-lookup"><span data-stu-id="a3486-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3486-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="a3486-130">Specifica una matrice di oggetti di configurazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="a3486-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-131">-Force</span><span class="sxs-lookup"><span data-stu-id="a3486-131">-Force</span></span>
<span data-ttu-id="a3486-132">Indica che il cmdlet esegue un aggiornamento forzato.</span><span class="sxs-lookup"><span data-stu-id="a3486-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a3486-133">-InformationAction</span></span>
<span data-ttu-id="a3486-134">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a3486-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a3486-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3486-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3486-136">Continuare</span><span class="sxs-lookup"><span data-stu-id="a3486-136">Continue</span></span>
- <span data-ttu-id="a3486-137">Ignora</span><span class="sxs-lookup"><span data-stu-id="a3486-137">Ignore</span></span>
- <span data-ttu-id="a3486-138">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a3486-138">Inquire</span></span>
- <span data-ttu-id="a3486-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a3486-139">SilentlyContinue</span></span>
- <span data-ttu-id="a3486-140">Stop</span><span class="sxs-lookup"><span data-stu-id="a3486-140">Stop</span></span>
- <span data-ttu-id="a3486-141">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a3486-141">Suspend</span></span>

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

### <span data-ttu-id="a3486-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a3486-142">-InformationVariable</span></span>
<span data-ttu-id="a3486-143">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a3486-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a3486-144">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="a3486-144">-Label</span></span>
<span data-ttu-id="a3486-145">Specifica un'etichetta per la distribuzione aggiornata.</span><span class="sxs-lookup"><span data-stu-id="a3486-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-146">-Modalità</span><span class="sxs-lookup"><span data-stu-id="a3486-146">-Mode</span></span>
<span data-ttu-id="a3486-147">Specifica la modalità di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a3486-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="a3486-148">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a3486-148">Valid values are:</span></span> 

- <span data-ttu-id="a3486-149">Automatico</span><span class="sxs-lookup"><span data-stu-id="a3486-149">Auto</span></span> 
- <span data-ttu-id="a3486-150">Manuale</span><span class="sxs-lookup"><span data-stu-id="a3486-150">Manual</span></span> 
- <span data-ttu-id="a3486-151">Simultaneo</span><span class="sxs-lookup"><span data-stu-id="a3486-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="a3486-152">-NewStatus</span></span>
<span data-ttu-id="a3486-153">Specifica lo stato di destinazione per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="a3486-154">I valori validi sono: in corso e sospesi.</span><span class="sxs-lookup"><span data-stu-id="a3486-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-155">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="a3486-155">-Package</span></span>
<span data-ttu-id="a3486-156">Specifica il percorso completo di un file di pacchetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a3486-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-157">-Profile</span><span class="sxs-lookup"><span data-stu-id="a3486-157">-Profile</span></span>
<span data-ttu-id="a3486-158">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3486-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3486-159">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a3486-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3486-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a3486-160">-RoleName</span></span>
<span data-ttu-id="a3486-161">Specifica il nome del ruolo da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a3486-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a3486-162">-ServiceName</span></span>
<span data-ttu-id="a3486-163">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="a3486-164">-Slot</span></span>
<span data-ttu-id="a3486-165">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="a3486-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="a3486-166">I valori validi sono: produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="a3486-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-167">-Stato</span><span class="sxs-lookup"><span data-stu-id="a3486-167">-Status</span></span>
<span data-ttu-id="a3486-168">Specifica che questo cmdlet modifica lo stato della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-169">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="a3486-169">-Upgrade</span></span>
<span data-ttu-id="a3486-170">Specifica che questo cmdlet aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3486-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3486-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3486-171">CommonParameters</span></span>
<span data-ttu-id="a3486-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3486-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3486-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3486-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3486-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3486-174">INPUTS</span></span>

## <span data-ttu-id="a3486-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3486-175">OUTPUTS</span></span>

## <span data-ttu-id="a3486-176">Note</span><span class="sxs-lookup"><span data-stu-id="a3486-176">NOTES</span></span>

## <span data-ttu-id="a3486-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3486-177">RELATED LINKS</span></span>

[<span data-ttu-id="a3486-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a3486-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="a3486-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="a3486-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="a3486-180">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a3486-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="a3486-181">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a3486-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="a3486-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a3486-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="a3486-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="a3486-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


