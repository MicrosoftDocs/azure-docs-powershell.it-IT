---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508632"
---
# <span data-ttu-id="34915-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="34915-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="34915-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34915-102">SYNOPSIS</span></span>
<span data-ttu-id="34915-103">Consente il supporto per il monitoraggio dei sistemi SAP.</span><span class="sxs-lookup"><span data-stu-id="34915-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34915-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34915-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34915-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34915-105">DESCRIPTION</span></span>
<span data-ttu-id="34915-106">Il cmdlet **set-AzureRmVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio dei sistemi SAP installati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34915-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="34915-107">Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e lo rende individuabile per il sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="34915-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="34915-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34915-108">EXAMPLES</span></span>

### <span data-ttu-id="34915-109">Esempio 1: usare l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="34915-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="34915-110">Questo comando configura la macchina virtuale denominata Contoso-server per l'uso dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="34915-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="34915-111">Il comando specifica l'account di archiviazione denominato stdstorage.</span><span class="sxs-lookup"><span data-stu-id="34915-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="34915-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34915-112">PARAMETERS</span></span>

### <span data-ttu-id="34915-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34915-113">-DefaultProfile</span></span>
<span data-ttu-id="34915-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34915-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34915-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="34915-115">-DisableWAD</span></span>
<span data-ttu-id="34915-116">Indica che questo cmdlet non Abilita la diagnostica Azure per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34915-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="34915-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="34915-117">-EnableWAD</span></span>
<span data-ttu-id="34915-118">Se questo parametro è disponibile, unifiedgroup consentirà la diagnostica di Windows Azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34915-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="34915-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="34915-119">-OSType</span></span>
<span data-ttu-id="34915-120">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="34915-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="34915-121">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="34915-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="34915-122">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="34915-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="34915-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34915-123">-ResourceGroupName</span></span>
<span data-ttu-id="34915-124">Specifica il nome del gruppo di risorse della macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34915-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="34915-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="34915-125">-SkipStorage</span></span>
<span data-ttu-id="34915-126">Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34915-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="34915-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="34915-127">-VMName</span></span>
<span data-ttu-id="34915-128">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34915-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="34915-129">Questo cmdlet aggiunge l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="34915-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="34915-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="34915-130">-WADStorageAccountName</span></span>
<span data-ttu-id="34915-131">Specifica il nome dell'account di archiviazione usato da questo cmdlet per configurare l'estensione LinuxDiagnostics o IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="34915-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="34915-132">Se la macchina virtuale non usa un account di archiviazione standard, devi specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="34915-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="34915-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34915-133">CommonParameters</span></span>
<span data-ttu-id="34915-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34915-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34915-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34915-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34915-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34915-136">INPUTS</span></span>

## <span data-ttu-id="34915-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34915-137">OUTPUTS</span></span>

## <span data-ttu-id="34915-138">Note</span><span class="sxs-lookup"><span data-stu-id="34915-138">NOTES</span></span>

## <span data-ttu-id="34915-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34915-139">RELATED LINKS</span></span>

[<span data-ttu-id="34915-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="34915-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="34915-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="34915-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="34915-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="34915-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)

