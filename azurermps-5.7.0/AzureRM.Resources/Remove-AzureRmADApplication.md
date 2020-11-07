---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686687"
---
# <span data-ttu-id="d3d7e-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d3d7e-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="d3d7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d7e-103">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3d7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d7e-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d7e-106">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d3d7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="d3d7e-108">Eliminare l'applicazione AAD.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="d3d7e-109">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d3d7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="d3d7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d7e-111">-DefaultProfile</span></span>
<span data-ttu-id="d3d7e-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d3d7e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3d7e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d3d7e-113">-Force</span></span>
<span data-ttu-id="d3d7e-114">Passare a eliminare un'applicazione senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="d3d7e-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d3d7e-115">-ObjectId</span></span>
<span data-ttu-id="d3d7e-116">ID oggetto dell'applicazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d7e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3d7e-117">-Confirm</span></span>
<span data-ttu-id="d3d7e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d7e-119">-WhatIf</span></span>
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

### <span data-ttu-id="d3d7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d7e-120">CommonParameters</span></span>
<span data-ttu-id="d3d7e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d7e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d7e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d7e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3d7e-123">INPUTS</span></span>

### <span data-ttu-id="d3d7e-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3d7e-124">None</span></span>
<span data-ttu-id="d3d7e-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3d7e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d7e-126">OUTPUTS</span></span>

## <span data-ttu-id="d3d7e-127">Note</span><span class="sxs-lookup"><span data-stu-id="d3d7e-127">NOTES</span></span>
<span data-ttu-id="d3d7e-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="d3d7e-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d3d7e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d7e-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3d7e-130">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d3d7e-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="d3d7e-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d3d7e-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="d3d7e-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d3d7e-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="d3d7e-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3d7e-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

