---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508300"
---
# <span data-ttu-id="23f28-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="23f28-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="23f28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23f28-102">SYNOPSIS</span></span>
<span data-ttu-id="23f28-103">Controlla la configurazione dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="23f28-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23f28-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="23f28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23f28-105">DESCRIPTION</span></span>
<span data-ttu-id="23f28-106">Il cmdlet **test-AzureRmVMAEMExtension** controlla la configurazione dell'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="23f28-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="23f28-107">L'estensione AEM raccoglie i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="23f28-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="23f28-108">Questo cmdlet controlla se sono disponibili i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="23f28-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="23f28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23f28-109">EXAMPLES</span></span>

### <span data-ttu-id="23f28-110">Esempio 1: controllare la configurazione dell'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="23f28-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="23f28-111">Questo comando controlla la configurazione dell'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="23f28-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="23f28-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23f28-112">PARAMETERS</span></span>

### <span data-ttu-id="23f28-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="23f28-113">-OSType</span></span>
<span data-ttu-id="23f28-114">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23f28-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="23f28-115">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="23f28-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="23f28-116">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="23f28-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="23f28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f28-117">-ResourceGroupName</span></span>
<span data-ttu-id="23f28-118">Specifica il nome del gruppo di risorse della macchina virtuale controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f28-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="23f28-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="23f28-119">-SkipStorageCheck</span></span>
<span data-ttu-id="23f28-120">Indica che questo cmdlet ignora il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="23f28-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="23f28-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="23f28-121">-VMName</span></span>
<span data-ttu-id="23f28-122">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23f28-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="23f28-123">Questo cmdlet verifica l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="23f28-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="23f28-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="23f28-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="23f28-125">Specifica un periodo di timeout, in minuti, per il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="23f28-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f28-126">CommonParameters</span></span>
<span data-ttu-id="23f28-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f28-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f28-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23f28-129">INPUTS</span></span>

### <span data-ttu-id="23f28-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="23f28-130">None</span></span>
<span data-ttu-id="23f28-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="23f28-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23f28-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f28-132">OUTPUTS</span></span>

## <span data-ttu-id="23f28-133">Note</span><span class="sxs-lookup"><span data-stu-id="23f28-133">NOTES</span></span>

## <span data-ttu-id="23f28-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23f28-134">RELATED LINKS</span></span>

[<span data-ttu-id="23f28-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="23f28-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="23f28-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="23f28-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="23f28-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="23f28-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


