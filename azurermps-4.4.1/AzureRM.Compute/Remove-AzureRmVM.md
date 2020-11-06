---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519600"
---
# <span data-ttu-id="32719-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="32719-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32719-102">SYNOPSIS</span></span>
<span data-ttu-id="32719-103">Rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="32719-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32719-104">SYNTAX</span></span>

### <span data-ttu-id="32719-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32719-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32719-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="32719-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32719-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32719-107">DESCRIPTION</span></span>
<span data-ttu-id="32719-108">Il cmdlet **Remove-AzureRmVM** rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="32719-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="32719-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32719-109">EXAMPLES</span></span>

### <span data-ttu-id="32719-110">Esempio 1: rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="32719-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="32719-111">Questo comando rimuove la macchina virtuale denominata VirtualMachine07 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="32719-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="32719-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32719-112">PARAMETERS</span></span>

### <span data-ttu-id="32719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32719-113">-DefaultProfile</span></span>
<span data-ttu-id="32719-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32719-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32719-115">-Force</span><span class="sxs-lookup"><span data-stu-id="32719-115">-Force</span></span>
<span data-ttu-id="32719-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="32719-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32719-117">-ID</span><span class="sxs-lookup"><span data-stu-id="32719-117">-Id</span></span>
<span data-ttu-id="32719-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32719-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32719-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="32719-119">-Name</span></span>
<span data-ttu-id="32719-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="32719-120">The resource name.</span></span>

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

### <span data-ttu-id="32719-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32719-121">-ResourceGroupName</span></span>
<span data-ttu-id="32719-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32719-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32719-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32719-123">-Confirm</span></span>
<span data-ttu-id="32719-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32719-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32719-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32719-125">-WhatIf</span></span>
<span data-ttu-id="32719-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32719-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="32719-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32719-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32719-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32719-128">CommonParameters</span></span>
<span data-ttu-id="32719-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32719-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32719-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32719-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32719-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32719-131">INPUTS</span></span>

## <span data-ttu-id="32719-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32719-132">OUTPUTS</span></span>

## <span data-ttu-id="32719-133">Note</span><span class="sxs-lookup"><span data-stu-id="32719-133">NOTES</span></span>

## <span data-ttu-id="32719-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32719-134">RELATED LINKS</span></span>

[<span data-ttu-id="32719-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="32719-136">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="32719-137">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="32719-138">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="32719-139">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="32719-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="32719-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


