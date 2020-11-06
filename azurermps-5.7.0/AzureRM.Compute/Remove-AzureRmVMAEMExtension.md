---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514479"
---
# <span data-ttu-id="deb72-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="deb72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="deb72-102">SYNOPSIS</span></span>
<span data-ttu-id="deb72-103">Rimuove l'estensione AEM da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="deb72-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deb72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="deb72-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="deb72-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="deb72-105">DESCRIPTION</span></span>
<span data-ttu-id="deb72-106">Il cmdlet **Remove-AzureRmVMAEMExtension** rimuove l'estensione AEM (Azure Enhanced Monitoring) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="deb72-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="deb72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="deb72-107">EXAMPLES</span></span>

### <span data-ttu-id="deb72-108">Esempio 1: rimuovere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="deb72-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="deb72-109">Questo comando rimuove l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="deb72-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="deb72-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="deb72-110">PARAMETERS</span></span>

### <span data-ttu-id="deb72-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="deb72-111">-Name</span></span>
<span data-ttu-id="deb72-112">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="deb72-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="deb72-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="deb72-113">-OSType</span></span>
<span data-ttu-id="deb72-114">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="deb72-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="deb72-115">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="deb72-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="deb72-116">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="deb72-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="deb72-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb72-117">-ResourceGroupName</span></span>
<span data-ttu-id="deb72-118">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="deb72-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="deb72-119">Questo cmdlet rimuove l'estensione AEM da tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="deb72-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="deb72-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="deb72-120">-VMName</span></span>
<span data-ttu-id="deb72-121">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="deb72-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="deb72-122">Questo cmdlet consente di rimuovere l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="deb72-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="deb72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb72-123">CommonParameters</span></span>
<span data-ttu-id="deb72-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb72-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb72-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="deb72-126">INPUTS</span></span>

### <span data-ttu-id="deb72-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="deb72-127">None</span></span>
<span data-ttu-id="deb72-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="deb72-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="deb72-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="deb72-129">OUTPUTS</span></span>

## <span data-ttu-id="deb72-130">Note</span><span class="sxs-lookup"><span data-stu-id="deb72-130">NOTES</span></span>

## <span data-ttu-id="deb72-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="deb72-131">RELATED LINKS</span></span>

[<span data-ttu-id="deb72-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="deb72-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="deb72-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="deb72-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


