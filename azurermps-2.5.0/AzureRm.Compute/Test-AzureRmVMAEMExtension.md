---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867128"
---
# <span data-ttu-id="06674-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="06674-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="06674-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06674-102">SYNOPSIS</span></span>
<span data-ttu-id="06674-103">Controlla la configurazione dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="06674-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06674-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06674-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06674-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06674-105">DESCRIPTION</span></span>
<span data-ttu-id="06674-106">Il cmdlet **test-AzureRmVMAEMExtension** controlla la configurazione dell'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="06674-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="06674-107">L'estensione AEM raccoglie i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="06674-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="06674-108">Questo cmdlet controlla se sono disponibili i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="06674-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="06674-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06674-109">EXAMPLES</span></span>

### <span data-ttu-id="06674-110">Esempio 1: controllare la configurazione dell'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="06674-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="06674-111">Questo comando controlla la configurazione dell'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="06674-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="06674-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06674-112">PARAMETERS</span></span>

### <span data-ttu-id="06674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06674-113">-DefaultProfile</span></span>
<span data-ttu-id="06674-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06674-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06674-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="06674-115">-OSType</span></span>
<span data-ttu-id="06674-116">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06674-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="06674-117">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="06674-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="06674-118">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="06674-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="06674-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06674-119">-ResourceGroupName</span></span>
<span data-ttu-id="06674-120">Specifica il nome del gruppo di risorse della macchina virtuale controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06674-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="06674-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="06674-121">-SkipStorageCheck</span></span>
<span data-ttu-id="06674-122">Indica che questo cmdlet ignora il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="06674-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="06674-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="06674-123">-VMName</span></span>
<span data-ttu-id="06674-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06674-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="06674-125">Questo cmdlet verifica l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="06674-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="06674-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="06674-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="06674-127">Specifica un periodo di timeout, in minuti, per il controllo della configurazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="06674-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="06674-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06674-128">CommonParameters</span></span>
<span data-ttu-id="06674-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06674-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06674-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06674-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06674-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06674-131">INPUTS</span></span>

### <span data-ttu-id="06674-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06674-132">None</span></span>
<span data-ttu-id="06674-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="06674-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06674-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06674-134">OUTPUTS</span></span>

### <span data-ttu-id="06674-135">Microsoft. Azure. Commands. Compute. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="06674-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="06674-136">Note</span><span class="sxs-lookup"><span data-stu-id="06674-136">NOTES</span></span>

## <span data-ttu-id="06674-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06674-137">RELATED LINKS</span></span>

[<span data-ttu-id="06674-138">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="06674-138">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="06674-139">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="06674-139">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="06674-140">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="06674-140">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


