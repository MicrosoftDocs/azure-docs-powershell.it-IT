---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860322"
---
# <span data-ttu-id="815fb-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="815fb-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="815fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="815fb-102">SYNOPSIS</span></span>
<span data-ttu-id="815fb-103">Rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="815fb-103">Removes an application security group.</span></span>

## <span data-ttu-id="815fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="815fb-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="815fb-105">DESCRIPTION</span></span>
<span data-ttu-id="815fb-106">Il cmdlet **Remove-AzApplicationSecurityGroup** rimuove un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="815fb-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="815fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="815fb-107">EXAMPLES</span></span>

### <span data-ttu-id="815fb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="815fb-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="815fb-109">Questo comando Elimina un gruppo di sicurezza dell'applicazione denominato MyApplicationSecurityGrouo nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="815fb-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="815fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="815fb-110">PARAMETERS</span></span>

### <span data-ttu-id="815fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815fb-111">-DefaultProfile</span></span>
<span data-ttu-id="815fb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="815fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815fb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="815fb-113">-Force</span></span>
<span data-ttu-id="815fb-114">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="815fb-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="815fb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="815fb-115">-Name</span></span>
<span data-ttu-id="815fb-116">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="815fb-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="815fb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="815fb-117">-PassThru</span></span>
<span data-ttu-id="815fb-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="815fb-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="815fb-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="815fb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="815fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="815fb-121">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="815fb-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="815fb-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="815fb-122">-Confirm</span></span>
<span data-ttu-id="815fb-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="815fb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815fb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815fb-124">-WhatIf</span></span>
<span data-ttu-id="815fb-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="815fb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815fb-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="815fb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815fb-127">CommonParameters</span></span>
<span data-ttu-id="815fb-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815fb-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815fb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815fb-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="815fb-130">INPUTS</span></span>

### <span data-ttu-id="815fb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="815fb-131">System.String</span></span>

## <span data-ttu-id="815fb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="815fb-132">OUTPUTS</span></span>

### <span data-ttu-id="815fb-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="815fb-133">System.Object</span></span>

## <span data-ttu-id="815fb-134">Note</span><span class="sxs-lookup"><span data-stu-id="815fb-134">NOTES</span></span>

## <span data-ttu-id="815fb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="815fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="815fb-136">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="815fb-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="815fb-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="815fb-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
