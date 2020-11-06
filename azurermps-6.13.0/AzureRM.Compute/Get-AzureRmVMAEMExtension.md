---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3d4867e33fe388195904d31fa7e83abe26dde474
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511860"
---
# <span data-ttu-id="c8e71-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c8e71-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="c8e71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8e71-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e71-103">Ottiene informazioni sull'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="c8e71-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8e71-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8e71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8e71-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e71-106">Il cmdlet **Get-AzureRmVMAEMExtension** ottiene informazioni sull'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="c8e71-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="c8e71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8e71-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e71-108">Esempio 1: ottenere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="c8e71-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c8e71-109">Questo comando ottiene le informazioni per l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="c8e71-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c8e71-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8e71-110">PARAMETERS</span></span>

### <span data-ttu-id="c8e71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e71-111">-DefaultProfile</span></span>
<span data-ttu-id="c8e71-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8e71-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8e71-113">-Name</span></span>
<span data-ttu-id="c8e71-114">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e71-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c8e71-115">Questo cmdlet consente di ottenere informazioni sull'estensione AEM nella macchina virtuale specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e71-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e71-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="c8e71-116">-OSType</span></span>
<span data-ttu-id="c8e71-117">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8e71-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c8e71-118">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c8e71-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c8e71-119">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="c8e71-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e71-120">-ResourceGroupName</span></span>
<span data-ttu-id="c8e71-121">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e71-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="c8e71-122">Questo cmdlet recupera le informazioni per l'estensione AEM in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e71-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="c8e71-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="c8e71-123">-Status</span></span>
<span data-ttu-id="c8e71-124">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="c8e71-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e71-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="c8e71-125">-VMName</span></span>
<span data-ttu-id="c8e71-126">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e71-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c8e71-127">Questo cmdlet ottiene informazioni sull'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c8e71-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c8e71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e71-128">CommonParameters</span></span>
<span data-ttu-id="c8e71-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e71-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e71-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e71-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8e71-131">INPUTS</span></span>

### <span data-ttu-id="c8e71-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e71-132">System.String</span></span>

### <span data-ttu-id="c8e71-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8e71-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8e71-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8e71-134">OUTPUTS</span></span>

### <span data-ttu-id="c8e71-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c8e71-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="c8e71-136">Note</span><span class="sxs-lookup"><span data-stu-id="c8e71-136">NOTES</span></span>

## <span data-ttu-id="c8e71-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8e71-137">RELATED LINKS</span></span>

[<span data-ttu-id="c8e71-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c8e71-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c8e71-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c8e71-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c8e71-140">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c8e71-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


