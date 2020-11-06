---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: df38df4da3fada0e89f527e7655c5c62c0df2602
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508708"
---
# <span data-ttu-id="eeea5-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eeea5-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="eeea5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeea5-102">SYNOPSIS</span></span>
<span data-ttu-id="eeea5-103">Rimuove l'estensione dello chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eeea5-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeea5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeea5-104">SYNTAX</span></span>

### <span data-ttu-id="eeea5-105">Linux</span><span class="sxs-lookup"><span data-stu-id="eeea5-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeea5-106">Windows</span><span class="sxs-lookup"><span data-stu-id="eeea5-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeea5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeea5-107">DESCRIPTION</span></span>
<span data-ttu-id="eeea5-108">Il cmdlet **Remove-AzureVMChefExtension** rimuove l'estensione chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eeea5-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="eeea5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeea5-109">EXAMPLES</span></span>

### <span data-ttu-id="eeea5-110">Esempio 1: rimuovere un'estensione dello chef da una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="eeea5-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="eeea5-111">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="eeea5-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="eeea5-112">Esempio 2: rimuovere un'estensione dello chef da una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="eeea5-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="eeea5-113">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="eeea5-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="eeea5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeea5-114">PARAMETERS</span></span>

### <span data-ttu-id="eeea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeea5-115">-DefaultProfile</span></span>
<span data-ttu-id="eeea5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeea5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeea5-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="eeea5-117">-Linux</span></span>
<span data-ttu-id="eeea5-118">Indica che questo cmdlet è destinato a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="eeea5-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeea5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeea5-119">-Name</span></span>
<span data-ttu-id="eeea5-120">Specifica il nome dell'estensione dello chef rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeea5-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eeea5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeea5-121">-ResourceGroupName</span></span>
<span data-ttu-id="eeea5-122">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eeea5-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="eeea5-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="eeea5-123">-VMName</span></span>
<span data-ttu-id="eeea5-124">Specifica il nome di una macchina virtuale per cui questo cmdlet rimuove l'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="eeea5-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="eeea5-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="eeea5-125">-Windows</span></span>
<span data-ttu-id="eeea5-126">Indica che questo cmdlet è destinato a una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="eeea5-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeea5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eeea5-127">-Confirm</span></span>
<span data-ttu-id="eeea5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeea5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeea5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeea5-129">-WhatIf</span></span>
<span data-ttu-id="eeea5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeea5-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="eeea5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeea5-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeea5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeea5-132">CommonParameters</span></span>
<span data-ttu-id="eeea5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeea5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeea5-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeea5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeea5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeea5-135">INPUTS</span></span>

## <span data-ttu-id="eeea5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeea5-136">OUTPUTS</span></span>

## <span data-ttu-id="eeea5-137">Note</span><span class="sxs-lookup"><span data-stu-id="eeea5-137">NOTES</span></span>

## <span data-ttu-id="eeea5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeea5-138">RELATED LINKS</span></span>

[<span data-ttu-id="eeea5-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eeea5-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="eeea5-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eeea5-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
