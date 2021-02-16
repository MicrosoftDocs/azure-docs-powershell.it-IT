---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177455"
---
# <span data-ttu-id="bfac6-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bfac6-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="bfac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfac6-102">SYNOPSIS</span></span>
<span data-ttu-id="bfac6-103">Controlla la configurazione dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="bfac6-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="bfac6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfac6-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfac6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfac6-105">DESCRIPTION</span></span>
<span data-ttu-id="bfac6-106">Il **cmdlet Test-AzVMAEMExtension** controlla la configurazione dell'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="bfac6-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="bfac6-107">L'estensione AEM raccoglie i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="bfac6-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="bfac6-108">Questo cmdlet controlla se i dati sulle prestazioni sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="bfac6-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="bfac6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfac6-109">EXAMPLES</span></span>

### <span data-ttu-id="bfac6-110">Esempio 1: Controllare la configurazione dell'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="bfac6-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="bfac6-111">Questo comando controlla la configurazione dell'estensione AEM per la macchina virtuale denominata contoso-server.</span><span class="sxs-lookup"><span data-stu-id="bfac6-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="bfac6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfac6-112">PARAMETERS</span></span>

### <span data-ttu-id="bfac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfac6-113">-DefaultProfile</span></span>
<span data-ttu-id="bfac6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfac6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfac6-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="bfac6-115">-OSType</span></span>
<span data-ttu-id="bfac6-116">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bfac6-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="bfac6-117">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bfac6-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="bfac6-118">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="bfac6-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="bfac6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfac6-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfac6-120">Specifica il nome del gruppo di risorse della macchina virtuale a cui controlla questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfac6-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="bfac6-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="bfac6-121">-SkipStorageCheck</span></span>
<span data-ttu-id="bfac6-122">Indica che questo cmdlet ignora il controllo della configurazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bfac6-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="bfac6-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfac6-123">-VMName</span></span>
<span data-ttu-id="bfac6-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfac6-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bfac6-125">Questo cmdlet testa l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bfac6-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfac6-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="bfac6-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="bfac6-127">Specifica un periodo di timeout, in minuti, per il controllo della configurazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bfac6-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="bfac6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfac6-128">CommonParameters</span></span>
<span data-ttu-id="bfac6-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfac6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfac6-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfac6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfac6-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfac6-131">INPUTS</span></span>

### <span data-ttu-id="bfac6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bfac6-132">System.String</span></span>

## <span data-ttu-id="bfac6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfac6-133">OUTPUTS</span></span>

### <span data-ttu-id="bfac6-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="bfac6-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="bfac6-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfac6-135">NOTES</span></span>

## <span data-ttu-id="bfac6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfac6-136">RELATED LINKS</span></span>

[<span data-ttu-id="bfac6-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bfac6-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="bfac6-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bfac6-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="bfac6-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="bfac6-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


