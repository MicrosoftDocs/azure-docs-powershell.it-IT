---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94023023"
---
# <span data-ttu-id="f2965-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2965-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="f2965-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2965-102">SYNOPSIS</span></span>
<span data-ttu-id="f2965-103">Ottiene informazioni sull'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="f2965-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="f2965-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2965-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2965-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2965-105">DESCRIPTION</span></span>
<span data-ttu-id="f2965-106">Il cmdlet **Get-AzVMAEMExtension** ottiene informazioni sull'estensione AEM (Azure Enhanced Monitoring).</span><span class="sxs-lookup"><span data-stu-id="f2965-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="f2965-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2965-107">EXAMPLES</span></span>

### <span data-ttu-id="f2965-108">Esempio 1: ottenere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="f2965-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f2965-109">Questo comando ottiene le informazioni per l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="f2965-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f2965-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2965-110">PARAMETERS</span></span>

### <span data-ttu-id="f2965-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2965-111">-DefaultProfile</span></span>
<span data-ttu-id="f2965-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2965-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2965-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2965-113">-Name</span></span>
<span data-ttu-id="f2965-114">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2965-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f2965-115">Questo cmdlet consente di ottenere informazioni sull'estensione AEM nella macchina virtuale specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2965-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="f2965-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="f2965-116">-OSType</span></span>
<span data-ttu-id="f2965-117">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f2965-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f2965-118">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f2965-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f2965-119">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f2965-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f2965-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2965-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2965-121">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2965-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="f2965-122">Questo cmdlet recupera le informazioni per l'estensione AEM in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2965-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="f2965-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="f2965-123">-Status</span></span>
<span data-ttu-id="f2965-124">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="f2965-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="f2965-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2965-125">-VMName</span></span>
<span data-ttu-id="f2965-126">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2965-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f2965-127">Questo cmdlet ottiene informazioni sull'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f2965-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2965-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2965-128">CommonParameters</span></span>
<span data-ttu-id="f2965-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2965-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2965-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2965-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2965-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2965-131">INPUTS</span></span>

### <span data-ttu-id="f2965-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f2965-132">System.String</span></span>

### <span data-ttu-id="f2965-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f2965-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2965-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2965-134">OUTPUTS</span></span>

### <span data-ttu-id="f2965-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f2965-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f2965-136">Note</span><span class="sxs-lookup"><span data-stu-id="f2965-136">NOTES</span></span>

## <span data-ttu-id="f2965-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2965-137">RELATED LINKS</span></span>

[<span data-ttu-id="f2965-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2965-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="f2965-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2965-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="f2965-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f2965-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


