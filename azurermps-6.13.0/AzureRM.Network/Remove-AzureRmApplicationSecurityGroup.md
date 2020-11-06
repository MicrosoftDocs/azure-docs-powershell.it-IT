---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: a1d0935e7ca61d5eee3055ad9751fd794e093e8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509208"
---
# <span data-ttu-id="44967-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44967-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="44967-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44967-102">SYNOPSIS</span></span>
<span data-ttu-id="44967-103">Rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44967-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44967-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44967-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44967-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44967-105">DESCRIPTION</span></span>
<span data-ttu-id="44967-106">Il cmdlet **Remove-AzureRmApplicationSecurityGroup** rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44967-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="44967-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44967-107">EXAMPLES</span></span>

### <span data-ttu-id="44967-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44967-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="44967-109">Questo comando Elimina un gruppo di sicurezza dell'applicazione denominato MyApplicationSecurityGrouo nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="44967-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="44967-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44967-110">PARAMETERS</span></span>

### <span data-ttu-id="44967-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44967-111">-AsJob</span></span>
<span data-ttu-id="44967-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44967-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44967-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44967-113">-DefaultProfile</span></span>
<span data-ttu-id="44967-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44967-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44967-115">-Force</span><span class="sxs-lookup"><span data-stu-id="44967-115">-Force</span></span>
<span data-ttu-id="44967-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="44967-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="44967-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="44967-117">-Name</span></span>
<span data-ttu-id="44967-118">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44967-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="44967-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44967-119">-PassThru</span></span>
<span data-ttu-id="44967-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="44967-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="44967-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="44967-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44967-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44967-122">-ResourceGroupName</span></span>
<span data-ttu-id="44967-123">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44967-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="44967-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44967-124">-Confirm</span></span>
<span data-ttu-id="44967-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44967-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44967-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44967-126">-WhatIf</span></span>
<span data-ttu-id="44967-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44967-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44967-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44967-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44967-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44967-129">CommonParameters</span></span>
<span data-ttu-id="44967-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44967-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44967-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44967-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44967-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44967-132">INPUTS</span></span>

### <span data-ttu-id="44967-133">System. String</span><span class="sxs-lookup"><span data-stu-id="44967-133">System.String</span></span>

## <span data-ttu-id="44967-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44967-134">OUTPUTS</span></span>

### <span data-ttu-id="44967-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44967-135">System.Boolean</span></span>

## <span data-ttu-id="44967-136">Note</span><span class="sxs-lookup"><span data-stu-id="44967-136">NOTES</span></span>

## <span data-ttu-id="44967-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44967-137">RELATED LINKS</span></span>

[<span data-ttu-id="44967-138">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44967-138">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="44967-139">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44967-139">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
