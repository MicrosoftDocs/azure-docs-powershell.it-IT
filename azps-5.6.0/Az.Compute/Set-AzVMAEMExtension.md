---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 4784df2e4ab6d24923bb4c7619e18459101bdf41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004573"
---
# <span data-ttu-id="ad5e5-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ad5e5-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="ad5e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5e5-103">Abilita il supporto per il monitoraggio per i sistemi SAP.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="ad5e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad5e5-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad5e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad5e5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad5e5-106">Il cmdlet **Set-AzVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio per i sistemi SAP installati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="ad5e5-107">Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e li rende individuabili per il sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="ad5e5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad5e5-108">EXAMPLES</span></span>

### <span data-ttu-id="ad5e5-109">Esempio 1: Usare l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="ad5e5-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="ad5e5-110">Questo comando configura la macchina virtuale denominata contoso-server in modo che usi l'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="ad5e5-111">Il comando specifica l'account di archiviazione denominato stdstorage.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="ad5e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad5e5-112">PARAMETERS</span></span>

### <span data-ttu-id="ad5e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5e5-113">-DefaultProfile</span></span>
<span data-ttu-id="ad5e5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5e5-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="ad5e5-115">-EnableWAD</span></span>
<span data-ttu-id="ad5e5-116">Se si specifica questo parametro, il commandlet abiliterà Windows Azure diagnostica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="ad5e5-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="ad5e5-117">-InstallNewExtension</span></span>
<span data-ttu-id="ad5e5-118">Installare la nuova estensione della macchina virtuale per SAP.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-118">Install the new VM Extension for SAP.</span></span>

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

### <span data-ttu-id="ad5e5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad5e5-119">-NoWait</span></span>
<span data-ttu-id="ad5e5-120">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ad5e5-121">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ad5e5-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="ad5e5-122">-OSType</span></span>
<span data-ttu-id="ad5e5-123">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ad5e5-124">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ad5e5-125">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="ad5e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad5e5-127">Specifica il nome del gruppo di risorse della macchina virtuale modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ad5e5-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="ad5e5-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="ad5e5-129">Imposta l'accesso all'identità della macchina virtuale sulle singole risorse, ad esempio i dischi di dati anziché l'completo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

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

### <span data-ttu-id="ad5e5-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="ad5e5-130">-SkipStorage</span></span>
<span data-ttu-id="ad5e5-131">Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="ad5e5-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad5e5-132">-VMName</span></span>
<span data-ttu-id="ad5e5-133">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ad5e5-134">Questo cmdlet aggiunge l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ad5e5-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad5e5-135">-WADStorageAccountName</span></span>
<span data-ttu-id="ad5e5-136">Specifica il nome dell'account di archiviazione che questo cmdlet usa per configurare l'estensione IaaSDiagnostics o LinuxDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="ad5e5-137">Se la macchina virtuale non usa un account di archiviazione standard, è necessario specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="ad5e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5e5-138">CommonParameters</span></span>
<span data-ttu-id="ad5e5-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5e5-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5e5-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e5-141">INPUTS</span></span>

### <span data-ttu-id="ad5e5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ad5e5-142">System.String</span></span>

## <span data-ttu-id="ad5e5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e5-143">OUTPUTS</span></span>

### <span data-ttu-id="ad5e5-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ad5e5-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ad5e5-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad5e5-145">NOTES</span></span>

## <span data-ttu-id="ad5e5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad5e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad5e5-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ad5e5-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="ad5e5-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ad5e5-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="ad5e5-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ad5e5-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


