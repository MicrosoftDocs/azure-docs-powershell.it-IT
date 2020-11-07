---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686684"
---
# <span data-ttu-id="c7f76-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c7f76-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="c7f76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7f76-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f76-103">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7f76-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7f76-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7f76-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f76-106">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7f76-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c7f76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7f76-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f76-108">Eliminare l'entità servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="c7f76-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="c7f76-109">Elimina l'entità di servizio di Azure Active Directory specificata.</span><span class="sxs-lookup"><span data-stu-id="c7f76-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="c7f76-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7f76-110">PARAMETERS</span></span>

### <span data-ttu-id="c7f76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f76-111">-DefaultProfile</span></span>
<span data-ttu-id="c7f76-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c7f76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7f76-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c7f76-113">-Force</span></span>
<span data-ttu-id="c7f76-114">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="c7f76-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="c7f76-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7f76-115">-ObjectId</span></span>
<span data-ttu-id="c7f76-116">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c7f76-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f76-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7f76-117">-PassThru</span></span>
<span data-ttu-id="c7f76-118">Se specificato, restituisce l'entità di servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="c7f76-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="c7f76-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7f76-119">-Confirm</span></span>
<span data-ttu-id="c7f76-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7f76-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f76-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f76-121">-WhatIf</span></span>
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

### <span data-ttu-id="c7f76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f76-122">CommonParameters</span></span>
<span data-ttu-id="c7f76-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f76-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f76-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f76-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7f76-125">INPUTS</span></span>

### <span data-ttu-id="c7f76-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c7f76-126">None</span></span>
<span data-ttu-id="c7f76-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c7f76-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7f76-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7f76-128">OUTPUTS</span></span>

### <span data-ttu-id="c7f76-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c7f76-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c7f76-130">Note</span><span class="sxs-lookup"><span data-stu-id="c7f76-130">NOTES</span></span>
<span data-ttu-id="c7f76-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="c7f76-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c7f76-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7f76-132">RELATED LINKS</span></span>

[<span data-ttu-id="c7f76-133">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c7f76-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c7f76-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c7f76-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c7f76-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c7f76-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c7f76-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7f76-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="c7f76-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7f76-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
