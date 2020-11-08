---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030813"
---
# <span data-ttu-id="06465-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06465-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="06465-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06465-102">SYNOPSIS</span></span>
<span data-ttu-id="06465-103">Configura l'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06465-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="06465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06465-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06465-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06465-105">DESCRIPTION</span></span>
<span data-ttu-id="06465-106">Il cmdlet **set-AzureVMDscExtension** configura l'estensione di configurazione dello stato (DSC) desiderata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06465-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="06465-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06465-107">EXAMPLES</span></span>

### <span data-ttu-id="06465-108">Esempio 1: configurare l'estensione DSC in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="06465-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="06465-109">Questo comando configura l'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06465-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="06465-110">Il pacchetto MyConfiguration.ps1.zip deve essere stato caricato in precedenza in Azure storage tramite il comando **Publish-AzureVMDscConfiguration** e include lo script MyConfiguration.ps1 e i moduli da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="06465-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="06465-111">L'argomento configurazione indica la configurazione DSC specifica nello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="06465-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="06465-112">Il parametro- *ConfigurationArgument* specifica una tabella hash con gli argomenti passati alla funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="06465-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="06465-113">Esempio 2: configurare l'estensione DSC in una macchina virtuale usando un percorso per i dati di configurazione</span><span class="sxs-lookup"><span data-stu-id="06465-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="06465-114">Questo comando configura l'estensione DSC in una macchina virtuale usando un percorso per i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="06465-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="06465-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06465-115">PARAMETERS</span></span>

### <span data-ttu-id="06465-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="06465-116">-ConfigurationArchive</span></span>
<span data-ttu-id="06465-117">Specifica il nome del pacchetto di configurazione (file con estensione zip) caricato in precedenza da Publish-AzureVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06465-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="06465-118">Questo parametro deve specificare solo il nome del file, senza alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="06465-118">This parameter must specify only the name of the file, without any path.</span></span>

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

### <span data-ttu-id="06465-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="06465-119">-ConfigurationArgument</span></span>
<span data-ttu-id="06465-120">Specifica una tabella hash che specifica gli argomenti della funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="06465-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="06465-121">Le chiavi corrispondono ai nomi dei parametri e ai valori per i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="06465-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="06465-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06465-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06465-123">tipi primitivi</span><span class="sxs-lookup"><span data-stu-id="06465-123">primitive types</span></span>
- <span data-ttu-id="06465-124">stringa</span><span class="sxs-lookup"><span data-stu-id="06465-124">string</span></span>
- <span data-ttu-id="06465-125">matrice</span><span class="sxs-lookup"><span data-stu-id="06465-125">array</span></span>
- <span data-ttu-id="06465-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="06465-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06465-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="06465-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="06465-128">Specifica il percorso di un file con estensione psd1 che specifica i dati per la funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="06465-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="06465-129">Questo file deve contenere un Hashtable come descritto in separare i dati di configurazione e ambiente https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="06465-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

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

### <span data-ttu-id="06465-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="06465-130">-ConfigurationName</span></span>
<span data-ttu-id="06465-131">Specifica il nome dello script di configurazione o del modulo richiamato dall'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="06465-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="06465-132">Il valore di questo parametro deve essere il nome di una delle funzioni di configurazione contenute negli script o nei moduli inclusi in *ConfigurationArchive*.</span><span class="sxs-lookup"><span data-stu-id="06465-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="06465-133">Questo cmdlet imposta come valore predefinito il nome del file assegnato dal parametro *ConfigurationArchive* se si omette questo parametro, escluse le eventuali estensioni.</span><span class="sxs-lookup"><span data-stu-id="06465-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="06465-134">Ad esempio, se *ConfigurationArchive* è "SalesWebSite.ps1.zip", il valore predefinito per *ConfigurationName* è "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="06465-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

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

### <span data-ttu-id="06465-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="06465-135">-ContainerName</span></span>
<span data-ttu-id="06465-136">Specifica il nome del contenitore di archiviazione di Azure in cui si trova il *ConfigurationArchive* .</span><span class="sxs-lookup"><span data-stu-id="06465-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

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

### <span data-ttu-id="06465-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="06465-137">-DataCollection</span></span>
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

### <span data-ttu-id="06465-138">-Force</span><span class="sxs-lookup"><span data-stu-id="06465-138">-Force</span></span>
<span data-ttu-id="06465-139">Indica che questo cmdlet sovrascrive i BLOB esistenti.</span><span class="sxs-lookup"><span data-stu-id="06465-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

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

### <span data-ttu-id="06465-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06465-140">-InformationAction</span></span>
<span data-ttu-id="06465-141">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="06465-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06465-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06465-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06465-143">Continuare</span><span class="sxs-lookup"><span data-stu-id="06465-143">Continue</span></span>
- <span data-ttu-id="06465-144">Ignora</span><span class="sxs-lookup"><span data-stu-id="06465-144">Ignore</span></span>
- <span data-ttu-id="06465-145">Informarsi</span><span class="sxs-lookup"><span data-stu-id="06465-145">Inquire</span></span>
- <span data-ttu-id="06465-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06465-146">SilentlyContinue</span></span>
- <span data-ttu-id="06465-147">Stop</span><span class="sxs-lookup"><span data-stu-id="06465-147">Stop</span></span>
- <span data-ttu-id="06465-148">Sospensione</span><span class="sxs-lookup"><span data-stu-id="06465-148">Suspend</span></span>

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

### <span data-ttu-id="06465-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06465-149">-InformationVariable</span></span>
<span data-ttu-id="06465-150">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="06465-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06465-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="06465-151">-Profile</span></span>
<span data-ttu-id="06465-152">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06465-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06465-153">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="06465-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06465-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="06465-154">-ReferenceName</span></span>
<span data-ttu-id="06465-155">Specifica una stringa definita dall'utente che può essere usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="06465-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="06465-156">Questo parametro viene specificato quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="06465-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="06465-157">Per gli aggiornamenti successivi, devi specificare il nome di riferimento usato in precedenza mentre aggiorni l'estensione.</span><span class="sxs-lookup"><span data-stu-id="06465-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="06465-158">Il *riferimento* assegnato a un'estensione viene restituito tramite il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="06465-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="06465-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="06465-159">-StorageContext</span></span>
<span data-ttu-id="06465-160">Specifica il contesto di archiviazione di Azure che fornisce le impostazioni di sicurezza usate per accedere allo script di configurazione.</span><span class="sxs-lookup"><span data-stu-id="06465-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="06465-161">Questo contesto fornisce l'accesso in lettura al contenitore specificato dal parametro *containerName* .</span><span class="sxs-lookup"><span data-stu-id="06465-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="06465-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="06465-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="06465-163">Specifica il suffisso DNS endpoint per tutti i servizi di archiviazione, ad esempio "core.contoso.net".</span><span class="sxs-lookup"><span data-stu-id="06465-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

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

### <span data-ttu-id="06465-164">-Versione</span><span class="sxs-lookup"><span data-stu-id="06465-164">-Version</span></span>
<span data-ttu-id="06465-165">Specifica la versione specifica dell'estensione DSC da usare.</span><span class="sxs-lookup"><span data-stu-id="06465-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="06465-166">Il valore predefinito è impostato su "1. \*" se questo parametro non è specificato.</span><span class="sxs-lookup"><span data-stu-id="06465-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

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

### <span data-ttu-id="06465-167">-VM</span><span class="sxs-lookup"><span data-stu-id="06465-167">-VM</span></span>
<span data-ttu-id="06465-168">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="06465-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06465-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="06465-169">-WmfVersion</span></span>
<span data-ttu-id="06465-170">Specifica la versione di Windows Management Framework (WMF) da installare nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06465-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="06465-171">L'estensione DSC dipende dalle caratteristiche DSC che sono disponibili solo negli aggiornamenti della WMF.</span><span class="sxs-lookup"><span data-stu-id="06465-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="06465-172">Questo parametro specifica la versione dell'aggiornamento da installare nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06465-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="06465-173">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06465-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06465-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="06465-174">4.0.</span></span>
<span data-ttu-id="06465-175">Installa WMF 4,0 a meno che non sia già installata una versione più recente.</span><span class="sxs-lookup"><span data-stu-id="06465-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="06465-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="06465-176">5.0.</span></span>
<span data-ttu-id="06465-177">Installa l'ultima versione di WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="06465-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="06465-178">più recente.</span><span class="sxs-lookup"><span data-stu-id="06465-178">latest.</span></span>
<span data-ttu-id="06465-179">Installa l'ultima WMF, attualmente WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="06465-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="06465-180">Il valore predefinito è il più recente.</span><span class="sxs-lookup"><span data-stu-id="06465-180">The default value is latest.</span></span>

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

### <span data-ttu-id="06465-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06465-181">-Confirm</span></span>
<span data-ttu-id="06465-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06465-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06465-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06465-183">-WhatIf</span></span>
<span data-ttu-id="06465-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06465-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06465-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06465-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06465-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06465-186">CommonParameters</span></span>
<span data-ttu-id="06465-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06465-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06465-188">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06465-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06465-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06465-189">INPUTS</span></span>

## <span data-ttu-id="06465-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06465-190">OUTPUTS</span></span>

## <span data-ttu-id="06465-191">Note</span><span class="sxs-lookup"><span data-stu-id="06465-191">NOTES</span></span>

## <span data-ttu-id="06465-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06465-192">RELATED LINKS</span></span>

[<span data-ttu-id="06465-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06465-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="06465-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06465-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="06465-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06465-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="06465-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06465-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="06465-197">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="06465-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


