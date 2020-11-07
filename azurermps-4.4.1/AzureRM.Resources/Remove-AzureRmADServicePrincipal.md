---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687088"
---
# <span data-ttu-id="2bf5c-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bf5c-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="2bf5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf5c-103">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bf5c-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bf5c-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf5c-106">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="2bf5c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bf5c-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf5c-108">--------------------------Eliminare l'entità servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="2bf5c-109">Elimina l'entità di servizio di Azure Active Directory specificata.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="2bf5c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bf5c-110">PARAMETERS</span></span>

### <span data-ttu-id="2bf5c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2bf5c-111">-Force</span></span>
<span data-ttu-id="2bf5c-112">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="2bf5c-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="2bf5c-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2bf5c-113">-ObjectId</span></span>
<span data-ttu-id="2bf5c-114">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf5c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bf5c-115">-PassThru</span></span>
<span data-ttu-id="2bf5c-116">Se specificato, restituisce l'entità di servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="2bf5c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bf5c-117">-Confirm</span></span>
<span data-ttu-id="2bf5c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf5c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf5c-119">-WhatIf</span></span>
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

### <span data-ttu-id="2bf5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf5c-120">-DefaultProfile</span></span>
<span data-ttu-id="2bf5c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bf5c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf5c-122">CommonParameters</span></span>
<span data-ttu-id="2bf5c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf5c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf5c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf5c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf5c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bf5c-125">INPUTS</span></span>

## <span data-ttu-id="2bf5c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bf5c-126">OUTPUTS</span></span>

### <span data-ttu-id="2bf5c-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bf5c-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2bf5c-128">Note</span><span class="sxs-lookup"><span data-stu-id="2bf5c-128">NOTES</span></span>
<span data-ttu-id="2bf5c-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="2bf5c-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2bf5c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bf5c-130">RELATED LINKS</span></span>

[<span data-ttu-id="2bf5c-131">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bf5c-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2bf5c-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bf5c-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2bf5c-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bf5c-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2bf5c-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2bf5c-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="2bf5c-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2bf5c-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
