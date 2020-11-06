---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 2e39f313e5f6d9c13a9eeb7f4365901ebbea4c9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512535"
---
# <span data-ttu-id="2a07b-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a07b-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="2a07b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a07b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a07b-103">Rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a07b-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a07b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a07b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a07b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a07b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a07b-106">Il cmdlet **Remove-AzureRmApplicationSecurityGroup** rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a07b-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="2a07b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a07b-107">EXAMPLES</span></span>

### <span data-ttu-id="2a07b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a07b-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2a07b-109">Questo comando Elimina un gruppo di sicurezza dell'applicazione denominato MyApplicationSecurityGrouo nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a07b-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2a07b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a07b-110">PARAMETERS</span></span>

### <span data-ttu-id="2a07b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a07b-111">-DefaultProfile</span></span>
<span data-ttu-id="2a07b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a07b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a07b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2a07b-113">-Force</span></span>
<span data-ttu-id="2a07b-114">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="2a07b-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2a07b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a07b-115">-Name</span></span>
<span data-ttu-id="2a07b-116">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a07b-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="2a07b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a07b-117">-PassThru</span></span>
<span data-ttu-id="2a07b-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2a07b-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2a07b-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2a07b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a07b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a07b-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a07b-121">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a07b-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="2a07b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a07b-122">-Confirm</span></span>
<span data-ttu-id="2a07b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a07b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a07b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a07b-124">-WhatIf</span></span>
<span data-ttu-id="2a07b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a07b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a07b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a07b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a07b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a07b-127">CommonParameters</span></span>
<span data-ttu-id="2a07b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a07b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a07b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a07b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a07b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a07b-130">INPUTS</span></span>

### <span data-ttu-id="2a07b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2a07b-131">System.String</span></span>

## <span data-ttu-id="2a07b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a07b-132">OUTPUTS</span></span>

### <span data-ttu-id="2a07b-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="2a07b-133">System.Object</span></span>

## <span data-ttu-id="2a07b-134">Note</span><span class="sxs-lookup"><span data-stu-id="2a07b-134">NOTES</span></span>

## <span data-ttu-id="2a07b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a07b-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a07b-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a07b-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="2a07b-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a07b-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
