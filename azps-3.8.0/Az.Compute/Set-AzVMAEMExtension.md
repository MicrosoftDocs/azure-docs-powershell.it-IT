---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019397"
---
# <span data-ttu-id="84272-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="84272-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="84272-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84272-102">SYNOPSIS</span></span>
<span data-ttu-id="84272-103">Consente il supporto per il monitoraggio dei sistemi SAP.</span><span class="sxs-lookup"><span data-stu-id="84272-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="84272-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84272-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84272-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84272-105">DESCRIPTION</span></span>
<span data-ttu-id="84272-106">Il cmdlet **set-AzVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio dei sistemi SAP installati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84272-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="84272-107">Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e lo rende individuabile per il sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="84272-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="84272-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84272-108">EXAMPLES</span></span>

### <span data-ttu-id="84272-109">Esempio 1: usare l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="84272-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="84272-110">Questo comando configura la macchina virtuale denominata Contoso-server per l'uso dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="84272-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="84272-111">Il comando specifica l'account di archiviazione denominato stdstorage.</span><span class="sxs-lookup"><span data-stu-id="84272-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="84272-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84272-112">PARAMETERS</span></span>

### <span data-ttu-id="84272-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84272-113">-DefaultProfile</span></span>
<span data-ttu-id="84272-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84272-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84272-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="84272-115">-EnableWAD</span></span>
<span data-ttu-id="84272-116">Se questo parametro è disponibile, unifiedgroup consentirà la diagnostica di Windows Azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84272-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="84272-117">-InstallNewExtension</span></span>
<span data-ttu-id="84272-118">Installare la nuova estensione VM per SAP.</span><span class="sxs-lookup"><span data-stu-id="84272-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="84272-119">-NoWait</span></span>
<span data-ttu-id="84272-120">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84272-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="84272-121">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="84272-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="84272-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="84272-122">-OSType</span></span>
<span data-ttu-id="84272-123">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="84272-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="84272-124">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84272-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="84272-125">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="84272-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84272-126">-ResourceGroupName</span></span>
<span data-ttu-id="84272-127">Specifica il nome del gruppo di risorse della macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84272-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="84272-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="84272-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="84272-129">Imposta l'accesso dell'identità VM alle singole risorse, ad esempio i dischi di dati anziché il gruppo di risorse completo.</span><span class="sxs-lookup"><span data-stu-id="84272-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="84272-130">-SkipStorage</span></span>
<span data-ttu-id="84272-131">Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84272-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="84272-132">-VMName</span></span>
<span data-ttu-id="84272-133">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84272-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="84272-134">Questo cmdlet aggiunge l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84272-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="84272-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84272-135">-WADStorageAccountName</span></span>
<span data-ttu-id="84272-136">Specifica il nome dell'account di archiviazione usato da questo cmdlet per configurare l'estensione LinuxDiagnostics o IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="84272-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="84272-137">Se la macchina virtuale non usa un account di archiviazione standard, devi specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84272-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84272-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84272-138">CommonParameters</span></span>
<span data-ttu-id="84272-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84272-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84272-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84272-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84272-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84272-141">INPUTS</span></span>

### <span data-ttu-id="84272-142">System. String</span><span class="sxs-lookup"><span data-stu-id="84272-142">System.String</span></span>

## <span data-ttu-id="84272-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84272-143">OUTPUTS</span></span>

### <span data-ttu-id="84272-144">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84272-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="84272-145">Note</span><span class="sxs-lookup"><span data-stu-id="84272-145">NOTES</span></span>

## <span data-ttu-id="84272-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84272-146">RELATED LINKS</span></span>

[<span data-ttu-id="84272-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="84272-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="84272-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="84272-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="84272-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="84272-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


