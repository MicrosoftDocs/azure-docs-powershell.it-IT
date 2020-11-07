---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: e75c34d76c304af272655c3e4e81fcfd547d11b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519599"
---
# <span data-ttu-id="1c89c-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1c89c-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="1c89c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c89c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c89c-103">Rimuove l'estensione AEM da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c89c-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c89c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c89c-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c89c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c89c-105">DESCRIPTION</span></span>
<span data-ttu-id="1c89c-106">Il cmdlet **Remove-AzureRmVMAEMExtension** rimuove l'estensione AEM (Azure Enhanced Monitoring) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c89c-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="1c89c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c89c-107">EXAMPLES</span></span>

### <span data-ttu-id="1c89c-108">Esempio 1: rimuovere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="1c89c-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="1c89c-109">Questo comando rimuove l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="1c89c-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="1c89c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c89c-110">PARAMETERS</span></span>

### <span data-ttu-id="1c89c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c89c-111">-DefaultProfile</span></span>
<span data-ttu-id="1c89c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c89c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c89c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c89c-113">-Name</span></span>
<span data-ttu-id="1c89c-114">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="1c89c-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="1c89c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="1c89c-115">-OSType</span></span>
<span data-ttu-id="1c89c-116">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1c89c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1c89c-117">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c89c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1c89c-118">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="1c89c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="1c89c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c89c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c89c-120">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c89c-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="1c89c-121">Questo cmdlet rimuove l'estensione AEM da tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c89c-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="1c89c-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="1c89c-122">-VMName</span></span>
<span data-ttu-id="1c89c-123">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1c89c-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1c89c-124">Questo cmdlet consente di rimuovere l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c89c-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c89c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c89c-125">CommonParameters</span></span>
<span data-ttu-id="1c89c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c89c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c89c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c89c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c89c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c89c-128">INPUTS</span></span>

## <span data-ttu-id="1c89c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c89c-129">OUTPUTS</span></span>

## <span data-ttu-id="1c89c-130">Note</span><span class="sxs-lookup"><span data-stu-id="1c89c-130">NOTES</span></span>

## <span data-ttu-id="1c89c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c89c-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c89c-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1c89c-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1c89c-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1c89c-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1c89c-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1c89c-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)

