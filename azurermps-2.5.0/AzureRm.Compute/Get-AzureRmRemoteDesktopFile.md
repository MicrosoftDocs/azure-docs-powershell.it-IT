---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866147"
---
# <span data-ttu-id="26720-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="26720-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="26720-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26720-102">SYNOPSIS</span></span>
<span data-ttu-id="26720-103">Ottiene un file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="26720-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26720-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26720-104">SYNTAX</span></span>

### <span data-ttu-id="26720-105">Scaricare</span><span class="sxs-lookup"><span data-stu-id="26720-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26720-106">Avvio</span><span class="sxs-lookup"><span data-stu-id="26720-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26720-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26720-107">DESCRIPTION</span></span>
<span data-ttu-id="26720-108">Il cmdlet **Get-AzureRmRemoteDesktopFile** ottiene un file con estensione RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="26720-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="26720-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26720-109">EXAMPLES</span></span>

### <span data-ttu-id="26720-110">Esempio 1: ottenere un file desktop remoto</span><span class="sxs-lookup"><span data-stu-id="26720-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="26720-111">Questo comando consente di ottenere il file desktop remoto per la macchina virtuale denominato VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="26720-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="26720-112">Il comando Archivia il risultato nel file denominato D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="26720-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="26720-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26720-113">PARAMETERS</span></span>

### <span data-ttu-id="26720-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26720-114">-DefaultProfile</span></span>
<span data-ttu-id="26720-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26720-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26720-116">-Avvio</span><span class="sxs-lookup"><span data-stu-id="26720-116">-Launch</span></span>
<span data-ttu-id="26720-117">Indica che questo cmdlet avvia Desktop remoto dopo avere ottenuto il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="26720-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="26720-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="26720-118">-LocalPath</span></span>
<span data-ttu-id="26720-119">Specifica il percorso completo locale in cui questo cmdlet archivia il file con estensione RDP.</span><span class="sxs-lookup"><span data-stu-id="26720-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="26720-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="26720-120">-Name</span></span>
<span data-ttu-id="26720-121">Specifica il nome del set di disponibilità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26720-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26720-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26720-122">-ResourceGroupName</span></span>
<span data-ttu-id="26720-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26720-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="26720-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26720-124">CommonParameters</span></span>
<span data-ttu-id="26720-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26720-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26720-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26720-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26720-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26720-127">INPUTS</span></span>

### <span data-ttu-id="26720-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="26720-128">None</span></span>
<span data-ttu-id="26720-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="26720-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26720-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26720-130">OUTPUTS</span></span>

## <span data-ttu-id="26720-131">Note</span><span class="sxs-lookup"><span data-stu-id="26720-131">NOTES</span></span>

## <span data-ttu-id="26720-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26720-132">RELATED LINKS</span></span>

