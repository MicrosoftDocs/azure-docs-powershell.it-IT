---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981054"
---
# <span data-ttu-id="c4306-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="c4306-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="c4306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4306-102">SYNOPSIS</span></span>
<span data-ttu-id="c4306-103">Ottiene un file con estensione rdp.</span><span class="sxs-lookup"><span data-stu-id="c4306-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="c4306-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4306-104">SYNTAX</span></span>

### <span data-ttu-id="c4306-105">Scarica</span><span class="sxs-lookup"><span data-stu-id="c4306-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4306-106">Avvia</span><span class="sxs-lookup"><span data-stu-id="c4306-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4306-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4306-107">DESCRIPTION</span></span>
<span data-ttu-id="c4306-108">Il cmdlet **Get-AzRemoteDesktopFile** ottiene un file RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="c4306-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="c4306-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4306-109">EXAMPLES</span></span>

### <span data-ttu-id="c4306-110">Esempio 1: Ottenere un file di Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="c4306-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="c4306-111">Questo comando recupera il file di Desktop remoto per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="c4306-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="c4306-112">Il comando archivia il risultato nel file denominato D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="c4306-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="c4306-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4306-113">PARAMETERS</span></span>

### <span data-ttu-id="c4306-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4306-114">-DefaultProfile</span></span>
<span data-ttu-id="c4306-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4306-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4306-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="c4306-116">-Launch</span></span>
<span data-ttu-id="c4306-117">Indica che questo cmdlet avvia Desktop remoto dopo averne eseguito il file rdp.</span><span class="sxs-lookup"><span data-stu-id="c4306-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4306-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="c4306-118">-LocalPath</span></span>
<span data-ttu-id="c4306-119">Specifica il percorso completo locale in cui questo cmdlet archivia il file con estensione rdp.</span><span class="sxs-lookup"><span data-stu-id="c4306-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4306-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c4306-120">-Name</span></span>
<span data-ttu-id="c4306-121">Specifica il nome del set di disponibilità che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4306-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c4306-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4306-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4306-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4306-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c4306-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4306-124">CommonParameters</span></span>
<span data-ttu-id="c4306-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4306-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4306-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4306-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4306-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4306-127">INPUTS</span></span>

### <span data-ttu-id="c4306-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c4306-128">System.String</span></span>

## <span data-ttu-id="c4306-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4306-129">OUTPUTS</span></span>

### <span data-ttu-id="c4306-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="c4306-130">System.Void</span></span>

## <span data-ttu-id="c4306-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4306-131">NOTES</span></span>

## <span data-ttu-id="c4306-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4306-132">RELATED LINKS</span></span>
