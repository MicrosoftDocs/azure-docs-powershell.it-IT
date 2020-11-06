---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518435"
---
# <span data-ttu-id="d6d8d-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d6d8d-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d6d8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d8d-103">Ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6d8d-104">SYNTAX</span></span>

### <span data-ttu-id="d6d8d-105">Ottenere tutti i gruppi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6d8d-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6d8d-106">Ottieni per ID gruppo</span><span class="sxs-lookup"><span data-stu-id="d6d8d-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6d8d-107">Trovare gruppi per utente</span><span class="sxs-lookup"><span data-stu-id="d6d8d-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6d8d-108">Trovare gruppi per prodotto</span><span class="sxs-lookup"><span data-stu-id="d6d8d-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6d8d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6d8d-109">DESCRIPTION</span></span>
<span data-ttu-id="d6d8d-110">Il cmdlet **Get-AzureRmApiManagementGroup** ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="d6d8d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6d8d-111">EXAMPLES</span></span>

### <span data-ttu-id="d6d8d-112">Esempio 1: ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="d6d8d-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="d6d8d-113">Questo comando consente di ottenere tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-113">This command gets all groups.</span></span>

### <span data-ttu-id="d6d8d-114">Esempio 2: ottenere un gruppo per ID</span><span class="sxs-lookup"><span data-stu-id="d6d8d-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="d6d8d-115">Questo comando consente di ottenere l'ID del gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="d6d8d-116">Esempio 3: ottenere un raggruppamento per nome</span><span class="sxs-lookup"><span data-stu-id="d6d8d-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="d6d8d-117">Questo comando ottiene il gruppo denominato Group0002.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="d6d8d-118">Esempio 4: ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="d6d8d-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="d6d8d-119">Questo comando consente di ottenere tutti i gruppi di utenti con l'ID utente denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="d6d8d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6d8d-120">PARAMETERS</span></span>

### <span data-ttu-id="d6d8d-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d6d8d-121">-Context</span></span>
<span data-ttu-id="d6d8d-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d8d-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d6d8d-123">-GroupId</span></span>
<span data-ttu-id="d6d8d-124">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-124">Specifies the group ID.</span></span>
<span data-ttu-id="d6d8d-125">Se specificato, il cmdlet cerca il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d8d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6d8d-126">-Name</span></span>
<span data-ttu-id="d6d8d-127">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-127">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d8d-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d6d8d-128">-ProductId</span></span>
<span data-ttu-id="d6d8d-129">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-129">Identifier of existing product.</span></span>
<span data-ttu-id="d6d8d-130">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="d6d8d-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d8d-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="d6d8d-132">-UserId</span></span>
<span data-ttu-id="d6d8d-133">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="d6d8d-134">Se specificato, il cmdlet restituirà tutti i gruppi a cui viene assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d8d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d8d-135">-DefaultProfile</span></span>
<span data-ttu-id="d6d8d-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6d8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d8d-137">CommonParameters</span></span>
<span data-ttu-id="d6d8d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d8d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6d8d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d8d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6d8d-140">INPUTS</span></span>

## <span data-ttu-id="d6d8d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6d8d-141">OUTPUTS</span></span>

### <span data-ttu-id="d6d8d-142">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="d6d8d-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="d6d8d-143">Note</span><span class="sxs-lookup"><span data-stu-id="d6d8d-143">NOTES</span></span>

## <span data-ttu-id="d6d8d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6d8d-144">RELATED LINKS</span></span>

[<span data-ttu-id="d6d8d-145">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d6d8d-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d6d8d-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d6d8d-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d6d8d-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d6d8d-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


