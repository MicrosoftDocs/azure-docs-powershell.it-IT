---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: 01eb8cba77177ca35f2e1b73ec410baa44e4a58c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865931"
---
# <span data-ttu-id="73d75-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="73d75-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="73d75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73d75-102">SYNOPSIS</span></span>
<span data-ttu-id="73d75-103">Consente il supporto per il monitoraggio dei sistemi SAP.</span><span class="sxs-lookup"><span data-stu-id="73d75-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73d75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73d75-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73d75-105">DESCRIPTION</span></span>
<span data-ttu-id="73d75-106">Il cmdlet **set-AzureRmVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio dei sistemi SAP installati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73d75-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="73d75-107">Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e lo rende individuabile per il sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="73d75-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="73d75-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73d75-108">EXAMPLES</span></span>

### <span data-ttu-id="73d75-109">Esempio 1: usare l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="73d75-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="73d75-110">Questo comando configura la macchina virtuale denominata Contoso-server per l'uso dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="73d75-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="73d75-111">Il comando specifica l'account di archiviazione denominato stdstorage.</span><span class="sxs-lookup"><span data-stu-id="73d75-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="73d75-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73d75-112">PARAMETERS</span></span>

### <span data-ttu-id="73d75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d75-113">-DefaultProfile</span></span>
<span data-ttu-id="73d75-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73d75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="73d75-115">-DisableWAD</span></span>
<span data-ttu-id="73d75-116">Indica che questo cmdlet non Abilita la diagnostica Azure per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73d75-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="73d75-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="73d75-117">-EnableWAD</span></span>
<span data-ttu-id="73d75-118">Se questo parametro è disponibile, unifiedgroup consentirà la diagnostica di Windows Azure per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73d75-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="73d75-119">-OSType</span></span>
<span data-ttu-id="73d75-120">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73d75-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="73d75-121">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73d75-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="73d75-122">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="73d75-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d75-123">-ResourceGroupName</span></span>
<span data-ttu-id="73d75-124">Specifica il nome del gruppo di risorse della macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73d75-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="73d75-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="73d75-125">-SkipStorage</span></span>
<span data-ttu-id="73d75-126">Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="73d75-126">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="73d75-127">-VMName</span></span>
<span data-ttu-id="73d75-128">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73d75-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="73d75-129">Questo cmdlet aggiunge l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73d75-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73d75-130">-WADStorageAccountName</span></span>
<span data-ttu-id="73d75-131">Specifica il nome dell'account di archiviazione usato da questo cmdlet per configurare l'estensione LinuxDiagnostics o IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="73d75-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="73d75-132">Se la macchina virtuale non usa un account di archiviazione standard, devi specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73d75-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d75-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d75-133">CommonParameters</span></span>
<span data-ttu-id="73d75-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d75-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d75-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d75-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d75-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73d75-136">INPUTS</span></span>

### <span data-ttu-id="73d75-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="73d75-137">None</span></span>
<span data-ttu-id="73d75-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="73d75-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73d75-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73d75-139">OUTPUTS</span></span>

### <span data-ttu-id="73d75-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="73d75-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="73d75-141">Note</span><span class="sxs-lookup"><span data-stu-id="73d75-141">NOTES</span></span>

## <span data-ttu-id="73d75-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73d75-142">RELATED LINKS</span></span>

[<span data-ttu-id="73d75-143">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="73d75-143">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="73d75-144">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="73d75-144">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="73d75-145">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="73d75-145">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


