---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: ed3215d6ae5b4e6386dc1ee9fce951f8b036d39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675172"
---
# <span data-ttu-id="03067-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03067-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="03067-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03067-102">SYNOPSIS</span></span>
<span data-ttu-id="03067-103">Configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="03067-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03067-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03067-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03067-105">DESCRIPTION</span></span>
<span data-ttu-id="03067-106">Il cmdlet **set-AzVMDiagnosticsExtension** configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="03067-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03067-107">EXAMPLES</span></span>

### <span data-ttu-id="03067-108">Esempio 1: abilitare la diagnostica usando un account di archiviazione specificato in un file di configurazione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="03067-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="03067-109">Questo comando usa un file di configurazione della diagnostica per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="03067-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="03067-110">Il file diagnostics_publicconfig.xml contiene la configurazione XML pubblica per l'estensione di diagnostica, incluso il nome dell'account di archiviazione a cui verranno inviati i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="03067-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="03067-111">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="03067-112">Esempio 2: abilitare la diagnostica usando un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="03067-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="03067-113">Questo comando usa il nome dell'account di archiviazione per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="03067-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="03067-114">Se la configurazione di diagnostica non specifica un nome dell'account di archiviazione o se si vuole ignorare il nome dell'account di archiviazione di diagnostica specificato nel file di configurazione, usare il parametro *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="03067-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="03067-115">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="03067-116">Esempio 3: abilitare la diagnostica tramite il nome e la chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="03067-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="03067-117">Questo comando usa il nome dell'account di archiviazione e la chiave per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="03067-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="03067-118">Se l'account di archiviazione diagnostica si trova in un abbonamento diverso rispetto alla macchina virtuale, abilitare l'invio dei dati di diagnostica all'account di archiviazione specificando esplicitamente il nome e la chiave.</span><span class="sxs-lookup"><span data-stu-id="03067-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="03067-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03067-119">PARAMETERS</span></span>

### <span data-ttu-id="03067-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="03067-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="03067-121">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="03067-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="03067-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03067-122">-DefaultProfile</span></span>
<span data-ttu-id="03067-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03067-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03067-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="03067-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="03067-125">Specifica il percorso del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="03067-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="03067-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03067-126">-Location</span></span>
<span data-ttu-id="03067-127">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="03067-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="03067-128">-Name</span></span>
<span data-ttu-id="03067-129">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="03067-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="03067-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="03067-130">-NoWait</span></span>
<span data-ttu-id="03067-131">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="03067-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="03067-132">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="03067-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="03067-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03067-133">-ResourceGroupName</span></span>
<span data-ttu-id="03067-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="03067-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="03067-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="03067-136">Specifica l'endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03067-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="03067-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="03067-137">-StorageAccountKey</span></span>
<span data-ttu-id="03067-138">Specifica la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03067-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="03067-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="03067-139">-StorageAccountName</span></span>
<span data-ttu-id="03067-140">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03067-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="03067-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="03067-141">-StorageContext</span></span>
<span data-ttu-id="03067-142">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03067-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="03067-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="03067-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="03067-144">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03067-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="03067-145">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="03067-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="03067-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="03067-146">-VMName</span></span>
<span data-ttu-id="03067-147">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03067-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="03067-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03067-148">CommonParameters</span></span>
<span data-ttu-id="03067-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03067-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03067-150">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03067-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03067-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03067-151">INPUTS</span></span>

### <span data-ttu-id="03067-152">System. String</span><span class="sxs-lookup"><span data-stu-id="03067-152">System.String</span></span>

### <span data-ttu-id="03067-153">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03067-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="03067-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03067-154">System.Boolean</span></span>

## <span data-ttu-id="03067-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03067-155">OUTPUTS</span></span>

### <span data-ttu-id="03067-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="03067-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="03067-157">Note</span><span class="sxs-lookup"><span data-stu-id="03067-157">NOTES</span></span>

## <span data-ttu-id="03067-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03067-158">RELATED LINKS</span></span>

[<span data-ttu-id="03067-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03067-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="03067-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="03067-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="03067-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03067-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

