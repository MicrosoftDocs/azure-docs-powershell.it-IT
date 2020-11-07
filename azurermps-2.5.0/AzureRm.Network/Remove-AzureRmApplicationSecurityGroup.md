---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866051"
---
# <span data-ttu-id="e8cc3-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8cc3-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="e8cc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cc3-103">Rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8cc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8cc3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8cc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="e8cc3-106">Il cmdlet **Remove-AzureRmApplicationSecurityGroup** rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="e8cc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="e8cc3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8cc3-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e8cc3-109">Questo comando Elimina un gruppo di sicurezza dell'applicazione denominato MyApplicationSecurityGrouo nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e8cc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8cc3-110">PARAMETERS</span></span>

### <span data-ttu-id="e8cc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cc3-111">-DefaultProfile</span></span>
<span data-ttu-id="e8cc3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8cc3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e8cc3-113">-Force</span></span>
<span data-ttu-id="e8cc3-114">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="e8cc3-114">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8cc3-115">-Name</span></span>
<span data-ttu-id="e8cc3-116">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8cc3-117">-PassThru</span></span>
<span data-ttu-id="e8cc3-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e8cc3-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cc3-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8cc3-121">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8cc3-122">-Confirm</span></span>
<span data-ttu-id="e8cc3-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8cc3-124">-WhatIf</span></span>
<span data-ttu-id="e8cc3-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8cc3-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8cc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cc3-127">CommonParameters</span></span>
<span data-ttu-id="e8cc3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8cc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cc3-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8cc3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cc3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8cc3-130">INPUTS</span></span>

### <span data-ttu-id="e8cc3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e8cc3-131">System.String</span></span>

## <span data-ttu-id="e8cc3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8cc3-132">OUTPUTS</span></span>

### <span data-ttu-id="e8cc3-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="e8cc3-133">System.Object</span></span>

## <span data-ttu-id="e8cc3-134">Note</span><span class="sxs-lookup"><span data-stu-id="e8cc3-134">NOTES</span></span>

## <span data-ttu-id="e8cc3-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8cc3-135">RELATED LINKS</span></span>

[<span data-ttu-id="e8cc3-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8cc3-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="e8cc3-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8cc3-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
