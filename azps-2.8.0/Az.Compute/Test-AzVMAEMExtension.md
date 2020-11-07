---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 7fe1219e9124a63784f3d064ffb25ed9d8271356
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675130"
---
# <span data-ttu-id="31b91-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="31b91-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="31b91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b91-102">SYNOPSIS</span></span>
<span data-ttu-id="31b91-103">Controlla la configurazione dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="31b91-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="31b91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b91-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31b91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b91-105">DESCRIPTION</span></span>
<span data-ttu-id="31b91-106">Il cmdlet **test-AzVMAEMExtension** controlla la configurazione dell'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="31b91-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="31b91-107">L'estensione AEM raccoglie i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="31b91-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="31b91-108">Questo cmdlet controlla se sono disponibili i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="31b91-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="31b91-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b91-109">EXAMPLES</span></span>

### <span data-ttu-id="31b91-110">Esempio 1: controllare la configurazione dell'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="31b91-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="31b91-111">Questo comando controlla la configurazione dell'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="31b91-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="31b91-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b91-112">PARAMETERS</span></span>

### <span data-ttu-id="31b91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b91-113">-DefaultProfile</span></span>
<span data-ttu-id="31b91-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b91-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="31b91-115">-OSType</span></span>
<span data-ttu-id="31b91-116">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31b91-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="31b91-117">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="31b91-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="31b91-118">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="31b91-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="31b91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b91-119">-ResourceGroupName</span></span>
<span data-ttu-id="31b91-120">Specifica il nome del gruppo di risorse della macchina virtuale controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b91-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="31b91-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="31b91-121">-SkipStorageCheck</span></span>
<span data-ttu-id="31b91-122">Indica che questo cmdlet ignora il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b91-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="31b91-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="31b91-123">-VMName</span></span>
<span data-ttu-id="31b91-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="31b91-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="31b91-125">Questo cmdlet verifica l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="31b91-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="31b91-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="31b91-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="31b91-127">Specifica un periodo di timeout, in minuti, per il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31b91-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b91-128">CommonParameters</span></span>
<span data-ttu-id="31b91-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b91-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31b91-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b91-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b91-131">INPUTS</span></span>

### <span data-ttu-id="31b91-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31b91-132">System.String</span></span>

## <span data-ttu-id="31b91-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b91-133">OUTPUTS</span></span>

### <span data-ttu-id="31b91-134">Microsoft. Azure. Commands. Compute. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="31b91-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="31b91-135">Note</span><span class="sxs-lookup"><span data-stu-id="31b91-135">NOTES</span></span>

## <span data-ttu-id="31b91-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b91-136">RELATED LINKS</span></span>

[<span data-ttu-id="31b91-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="31b91-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="31b91-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="31b91-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="31b91-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="31b91-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


