---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202539"
---
# <span data-ttu-id="78d94-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="78d94-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="78d94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78d94-102">SYNOPSIS</span></span>
<span data-ttu-id="78d94-103">Ottiene un file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="78d94-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="78d94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78d94-104">SYNTAX</span></span>

### <span data-ttu-id="78d94-105">Scaricare</span><span class="sxs-lookup"><span data-stu-id="78d94-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78d94-106">Avvio</span><span class="sxs-lookup"><span data-stu-id="78d94-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78d94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d94-107">DESCRIPTION</span></span>
<span data-ttu-id="78d94-108">Il cmdlet **Get-AzRemoteDesktopFile** ottiene un file con estensione RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="78d94-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="78d94-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78d94-109">EXAMPLES</span></span>

### <span data-ttu-id="78d94-110">Esempio 1: ottenere un file desktop remoto</span><span class="sxs-lookup"><span data-stu-id="78d94-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="78d94-111">Questo comando consente di ottenere il file desktop remoto per la macchina virtuale denominato VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="78d94-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="78d94-112">Il comando Archivia il risultato nel file denominato D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="78d94-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="78d94-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78d94-113">PARAMETERS</span></span>

### <span data-ttu-id="78d94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d94-114">-DefaultProfile</span></span>
<span data-ttu-id="78d94-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78d94-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d94-116">-Avvio</span><span class="sxs-lookup"><span data-stu-id="78d94-116">-Launch</span></span>
<span data-ttu-id="78d94-117">Indica che questo cmdlet avvia Desktop remoto dopo avere ottenuto il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="78d94-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="78d94-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="78d94-118">-LocalPath</span></span>
<span data-ttu-id="78d94-119">Specifica il percorso completo locale in cui questo cmdlet archivia il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="78d94-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="78d94-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="78d94-120">-Name</span></span>
<span data-ttu-id="78d94-121">Specifica il nome del set di disponibilità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d94-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78d94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d94-122">-ResourceGroupName</span></span>
<span data-ttu-id="78d94-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78d94-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78d94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d94-124">CommonParameters</span></span>
<span data-ttu-id="78d94-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d94-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d94-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d94-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78d94-127">INPUTS</span></span>

### <span data-ttu-id="78d94-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78d94-128">System.String</span></span>

## <span data-ttu-id="78d94-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78d94-129">OUTPUTS</span></span>

### <span data-ttu-id="78d94-130">System. void</span><span class="sxs-lookup"><span data-stu-id="78d94-130">System.Void</span></span>

## <span data-ttu-id="78d94-131">Note</span><span class="sxs-lookup"><span data-stu-id="78d94-131">NOTES</span></span>

## <span data-ttu-id="78d94-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78d94-132">RELATED LINKS</span></span>
