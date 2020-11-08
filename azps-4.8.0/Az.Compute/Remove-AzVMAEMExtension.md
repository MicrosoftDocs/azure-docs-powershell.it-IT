---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189132"
---
# <span data-ttu-id="0e257-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0e257-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="0e257-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e257-102">SYNOPSIS</span></span>
<span data-ttu-id="0e257-103">Rimuove l'estensione AEM da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e257-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="0e257-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e257-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e257-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e257-105">DESCRIPTION</span></span>
<span data-ttu-id="0e257-106">Il cmdlet **Remove-AzVMAEMExtension** rimuove l'estensione AEM (Azure Enhanced Monitoring) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e257-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="0e257-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e257-107">EXAMPLES</span></span>

### <span data-ttu-id="0e257-108">Esempio 1: rimuovere l'estensione AEM</span><span class="sxs-lookup"><span data-stu-id="0e257-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="0e257-109">Questo comando rimuove l'estensione AEM per la macchina virtuale denominata Contoso-server.</span><span class="sxs-lookup"><span data-stu-id="0e257-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="0e257-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e257-110">PARAMETERS</span></span>

### <span data-ttu-id="0e257-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e257-111">-DefaultProfile</span></span>
<span data-ttu-id="0e257-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e257-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e257-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e257-113">-Name</span></span>
<span data-ttu-id="0e257-114">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione AEM.</span><span class="sxs-lookup"><span data-stu-id="0e257-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="0e257-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="0e257-115">-NoWait</span></span>
<span data-ttu-id="0e257-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0e257-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0e257-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="0e257-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e257-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="0e257-118">-OSType</span></span>
<span data-ttu-id="0e257-119">Specifica il tipo di sistema operativo del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e257-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0e257-120">Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0e257-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0e257-121">I valori accettabili per questo parametro sono: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0e257-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0e257-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e257-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e257-123">Specifica il nome del gruppo di risorse di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e257-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="0e257-124">Questo cmdlet rimuove l'estensione AEM da tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e257-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="0e257-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e257-125">-VMName</span></span>
<span data-ttu-id="0e257-126">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e257-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0e257-127">Questo cmdlet consente di rimuovere l'estensione AEM per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0e257-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e257-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e257-128">CommonParameters</span></span>
<span data-ttu-id="0e257-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e257-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e257-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e257-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e257-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e257-131">INPUTS</span></span>

### <span data-ttu-id="0e257-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0e257-132">System.String</span></span>

## <span data-ttu-id="0e257-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e257-133">OUTPUTS</span></span>

### <span data-ttu-id="0e257-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0e257-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0e257-135">Note</span><span class="sxs-lookup"><span data-stu-id="0e257-135">NOTES</span></span>

## <span data-ttu-id="0e257-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e257-136">RELATED LINKS</span></span>

[<span data-ttu-id="0e257-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0e257-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="0e257-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0e257-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="0e257-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0e257-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


