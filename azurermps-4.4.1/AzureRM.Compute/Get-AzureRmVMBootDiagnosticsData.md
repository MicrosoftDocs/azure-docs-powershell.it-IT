---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: dfe9324644115d00054961e8e159c672d1aba588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522163"
---
# <span data-ttu-id="0ef3a-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0ef3a-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="0ef3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ef3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef3a-103">Ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ef3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ef3a-104">SYNTAX</span></span>

### <span data-ttu-id="0ef3a-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ef3a-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ef3a-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="0ef3a-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ef3a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ef3a-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef3a-108">Il cmdlet **Get-AzureRmVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="0ef3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ef3a-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef3a-110">Esempio 1: ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="0ef3a-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="0ef3a-111">Questo comando consente di ottenere i dati di diagnostica di avvio per la macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="0ef3a-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="0ef3a-113">Il comando Archivia i dati in un percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="0ef3a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ef3a-114">PARAMETERS</span></span>

### <span data-ttu-id="0ef3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef3a-115">-DefaultProfile</span></span>
<span data-ttu-id="0ef3a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ef3a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0ef3a-117">-Linux</span></span>
<span data-ttu-id="0ef3a-118">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef3a-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="0ef3a-119">-LocalPath</span></span>
<span data-ttu-id="0ef3a-120">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef3a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ef3a-121">-Name</span></span>
<span data-ttu-id="0ef3a-122">Specifica il nome della macchina virtuale per cui questo cmdlet ottiene i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef3a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef3a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ef3a-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0ef3a-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="0ef3a-125">-Windows</span></span>
<span data-ttu-id="0ef3a-126">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef3a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef3a-127">CommonParameters</span></span>
<span data-ttu-id="0ef3a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef3a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef3a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef3a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ef3a-130">INPUTS</span></span>

## <span data-ttu-id="0ef3a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ef3a-131">OUTPUTS</span></span>

## <span data-ttu-id="0ef3a-132">Note</span><span class="sxs-lookup"><span data-stu-id="0ef3a-132">NOTES</span></span>

## <span data-ttu-id="0ef3a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ef3a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0ef3a-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0ef3a-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


