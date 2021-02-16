---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199174"
---
# <span data-ttu-id="077e3-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="077e3-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="077e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077e3-102">SYNOPSIS</span></span>
<span data-ttu-id="077e3-103">Configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="077e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="077e3-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077e3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="077e3-105">DESCRIPTION</span></span>
<span data-ttu-id="077e3-106">Il cmdlet **Set-AzVMDiagnosticsExtension** configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="077e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="077e3-107">EXAMPLES</span></span>

### <span data-ttu-id="077e3-108">Esempio 1: Abilitare la diagnostica usando un account di archiviazione specificato in un file di configurazione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="077e3-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="077e3-109">Questo comando usa un file di configurazione di diagnostica per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="077e3-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="077e3-110">Il file diagnostics_publicconfig.xml contiene la configurazione XML pubblica per l'estensione di diagnostica, incluso il nome dell'account di archiviazione a cui verranno inviati i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="077e3-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="077e3-111">L'account di archiviazione di diagnostica deve essere nello stesso abbonamento della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="077e3-112">Esempio 2: Abilitare la diagnostica con il nome di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="077e3-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="077e3-113">Questo comando usa il nome dell'account di archiviazione per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="077e3-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="077e3-114">Se la configurazione di diagnostica non specifica il nome di un account di archiviazione o se si vuole ignorare il nome dell'account di archiviazione di diagnostica specificato nel file di configurazione, usare il *parametro StorageAccountName.*</span><span class="sxs-lookup"><span data-stu-id="077e3-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="077e3-115">L'account di archiviazione di diagnostica deve essere nello stesso abbonamento della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="077e3-116">Esempio 3: Abilitare la diagnostica usando il nome e la chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="077e3-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="077e3-117">Questo comando usa il nome dell'account di archiviazione e la chiave per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="077e3-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="077e3-118">Se l'account di archiviazione di diagnostica si trova in un abbonamento diverso da quello della macchina virtuale, abilitare l'invio dei dati di diagnostica a tale account di archiviazione specificando in modo esplicito il nome e la chiave.</span><span class="sxs-lookup"><span data-stu-id="077e3-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="077e3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="077e3-119">PARAMETERS</span></span>

### <span data-ttu-id="077e3-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="077e3-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="077e3-121">Indica se questo cmdlet consente all'agente guest di Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="077e3-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077e3-122">-DefaultProfile</span></span>
<span data-ttu-id="077e3-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="077e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="077e3-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="077e3-125">Specifica il percorso del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="077e3-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-126">-Location</span><span class="sxs-lookup"><span data-stu-id="077e3-126">-Location</span></span>
<span data-ttu-id="077e3-127">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="077e3-128">-Name</span></span>
<span data-ttu-id="077e3-129">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="077e3-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="077e3-130">-NoWait</span></span>
<span data-ttu-id="077e3-131">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="077e3-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="077e3-132">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="077e3-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077e3-133">-ResourceGroupName</span></span>
<span data-ttu-id="077e3-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="077e3-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="077e3-136">Specifica l'endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="077e3-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="077e3-137">-StorageAccountKey</span></span>
<span data-ttu-id="077e3-138">Specifica la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="077e3-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="077e3-139">-StorageAccountName</span></span>
<span data-ttu-id="077e3-140">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="077e3-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="077e3-141">-StorageContext</span></span>
<span data-ttu-id="077e3-142">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="077e3-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="077e3-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="077e3-144">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="077e3-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="077e3-145">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft.Compute per il parametro *PublisherName* e VMAccessAgent per il *parametro Type.*</span><span class="sxs-lookup"><span data-stu-id="077e3-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="077e3-146">-VMName</span></span>
<span data-ttu-id="077e3-147">Specifica il nome della macchina virtuale in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077e3-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077e3-148">CommonParameters</span></span>
<span data-ttu-id="077e3-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077e3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077e3-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="077e3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077e3-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="077e3-151">INPUTS</span></span>

### <span data-ttu-id="077e3-152">System.String</span><span class="sxs-lookup"><span data-stu-id="077e3-152">System.String</span></span>

### <span data-ttu-id="077e3-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="077e3-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="077e3-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="077e3-154">System.Boolean</span></span>

## <span data-ttu-id="077e3-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="077e3-155">OUTPUTS</span></span>

### <span data-ttu-id="077e3-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="077e3-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="077e3-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="077e3-157">NOTES</span></span>

## <span data-ttu-id="077e3-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="077e3-158">RELATED LINKS</span></span>

[<span data-ttu-id="077e3-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="077e3-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="077e3-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="077e3-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="077e3-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="077e3-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


