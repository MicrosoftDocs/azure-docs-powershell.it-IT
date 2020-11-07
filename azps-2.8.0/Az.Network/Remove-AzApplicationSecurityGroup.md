---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852790"
---
# <span data-ttu-id="58e28-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e28-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="58e28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58e28-102">SYNOPSIS</span></span>
<span data-ttu-id="58e28-103">Rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58e28-103">Removes an application security group.</span></span>

## <span data-ttu-id="58e28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e28-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e28-105">DESCRIPTION</span></span>
<span data-ttu-id="58e28-106">Il cmdlet **Remove-AzApplicationSecurityGroup** rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58e28-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="58e28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e28-107">EXAMPLES</span></span>

### <span data-ttu-id="58e28-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58e28-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="58e28-109">Questo comando Elimina un gruppo di sicurezza dell'applicazione denominato MyApplicationSecurityGrouo nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="58e28-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="58e28-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58e28-110">PARAMETERS</span></span>

### <span data-ttu-id="58e28-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58e28-111">-AsJob</span></span>
<span data-ttu-id="58e28-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="58e28-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58e28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e28-113">-DefaultProfile</span></span>
<span data-ttu-id="58e28-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e28-115">-Force</span><span class="sxs-lookup"><span data-stu-id="58e28-115">-Force</span></span>
<span data-ttu-id="58e28-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="58e28-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="58e28-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58e28-117">-Name</span></span>
<span data-ttu-id="58e28-118">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58e28-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e28-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58e28-119">-PassThru</span></span>
<span data-ttu-id="58e28-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="58e28-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="58e28-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="58e28-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58e28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e28-122">-ResourceGroupName</span></span>
<span data-ttu-id="58e28-123">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58e28-123">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e28-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58e28-124">-Confirm</span></span>
<span data-ttu-id="58e28-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58e28-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e28-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e28-126">-WhatIf</span></span>
<span data-ttu-id="58e28-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e28-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e28-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e28-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e28-129">CommonParameters</span></span>
<span data-ttu-id="58e28-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e28-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e28-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e28-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58e28-132">INPUTS</span></span>

### <span data-ttu-id="58e28-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58e28-133">System.String</span></span>

## <span data-ttu-id="58e28-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e28-134">OUTPUTS</span></span>

### <span data-ttu-id="58e28-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58e28-135">System.Boolean</span></span>

## <span data-ttu-id="58e28-136">Note</span><span class="sxs-lookup"><span data-stu-id="58e28-136">NOTES</span></span>

## <span data-ttu-id="58e28-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e28-137">RELATED LINKS</span></span>

[<span data-ttu-id="58e28-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e28-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="58e28-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e28-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
