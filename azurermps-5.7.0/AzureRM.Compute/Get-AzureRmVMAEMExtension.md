---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687944"
---
# <span data-ttu-id="ce9be-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ce9be-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ce9be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce9be-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9be-103">Ottiene informazioni sull'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="ce9be-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce9be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce9be-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ce9be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce9be-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9be-106">Il cmdlet **Get-AzureRmVMAEMExtension** ottiene informazioni sull'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="ce9be-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="ce9be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce9be-107">EXAMPLES</span></span>

### <span data-ttu-id="ce9be-108">Esempio 1: ottenere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="ce9be-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ce9be-109">Questo comando ottiene le informazioni per l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="ce9be-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ce9be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce9be-110">PARAMETERS</span></span>

### <span data-ttu-id="ce9be-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce9be-111">-Name</span></span>
<span data-ttu-id="ce9be-112">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce9be-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ce9be-113">Questo cmdlet consente di ottenere informazioni sull'estensione AEM nella macchina virtuale specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce9be-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9be-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="ce9be-114">-OSType</span></span>
<span data-ttu-id="ce9be-115">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ce9be-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ce9be-116">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ce9be-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ce9be-117">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ce9be-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9be-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce9be-119">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce9be-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ce9be-120">Questo cmdlet recupera le informazioni per l'estensione AEM in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce9be-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="ce9be-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="ce9be-121">-Status</span></span>
<span data-ttu-id="ce9be-122">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="ce9be-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9be-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="ce9be-123">-VMName</span></span>
<span data-ttu-id="ce9be-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce9be-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ce9be-125">Questo cmdlet ottiene informazioni sull'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ce9be-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce9be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9be-126">CommonParameters</span></span>
<span data-ttu-id="ce9be-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9be-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9be-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce9be-129">INPUTS</span></span>

### <span data-ttu-id="ce9be-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce9be-130">None</span></span>
<span data-ttu-id="ce9be-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ce9be-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce9be-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce9be-132">OUTPUTS</span></span>

## <span data-ttu-id="ce9be-133">Note</span><span class="sxs-lookup"><span data-stu-id="ce9be-133">NOTES</span></span>

## <span data-ttu-id="ce9be-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce9be-134">RELATED LINKS</span></span>

[<span data-ttu-id="ce9be-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ce9be-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ce9be-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ce9be-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ce9be-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ce9be-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


