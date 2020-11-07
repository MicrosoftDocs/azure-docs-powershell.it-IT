---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686219"
---
# <span data-ttu-id="a57a3-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="a57a3-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="a57a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a57a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a57a3-103">Ottiene un file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="a57a3-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a57a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a57a3-104">SYNTAX</span></span>

### <span data-ttu-id="a57a3-105">Scaricare</span><span class="sxs-lookup"><span data-stu-id="a57a3-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a57a3-106">Avvio</span><span class="sxs-lookup"><span data-stu-id="a57a3-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="a57a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a57a3-107">DESCRIPTION</span></span>
<span data-ttu-id="a57a3-108">Il cmdlet **Get-AzureRmRemoteDesktopFile** ottiene un file con estensione RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="a57a3-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="a57a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a57a3-109">EXAMPLES</span></span>

### <span data-ttu-id="a57a3-110">Esempio 1: ottenere un file desktop remoto</span><span class="sxs-lookup"><span data-stu-id="a57a3-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="a57a3-111">Questo comando consente di ottenere il file desktop remoto per la macchina virtuale denominato VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a57a3-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="a57a3-112">Il comando Archivia il risultato nel file denominato D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="a57a3-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="a57a3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a57a3-113">PARAMETERS</span></span>

### <span data-ttu-id="a57a3-114">-Avvio</span><span class="sxs-lookup"><span data-stu-id="a57a3-114">-Launch</span></span>
<span data-ttu-id="a57a3-115">Indica che questo cmdlet avvia Desktop remoto dopo avere ottenuto il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="a57a3-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="a57a3-116">-LocalPath</span></span>
<span data-ttu-id="a57a3-117">Specifica il percorso completo locale in cui questo cmdlet archivia il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="a57a3-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a57a3-118">-Name</span></span>
<span data-ttu-id="a57a3-119">Specifica il nome del set di disponibilità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57a3-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="a57a3-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a57a3-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a57a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57a3-122">CommonParameters</span></span>
<span data-ttu-id="a57a3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57a3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57a3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a57a3-125">INPUTS</span></span>

### <span data-ttu-id="a57a3-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a57a3-126">None</span></span>
<span data-ttu-id="a57a3-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a57a3-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a57a3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a57a3-128">OUTPUTS</span></span>

## <span data-ttu-id="a57a3-129">Note</span><span class="sxs-lookup"><span data-stu-id="a57a3-129">NOTES</span></span>

## <span data-ttu-id="a57a3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a57a3-130">RELATED LINKS</span></span>

