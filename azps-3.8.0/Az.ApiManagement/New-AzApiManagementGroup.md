---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 8f7d221ca4f90f67bce038015b4c654881dfa598
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020197"
---
# <span data-ttu-id="96928-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="96928-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="96928-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96928-102">SYNOPSIS</span></span>
<span data-ttu-id="96928-103">Crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="96928-103">Creates an API management group.</span></span>

## <span data-ttu-id="96928-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96928-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96928-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96928-105">DESCRIPTION</span></span>
<span data-ttu-id="96928-106">Il cmdlet **New-AzApiManagementGroup** crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="96928-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="96928-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96928-107">EXAMPLES</span></span>

### <span data-ttu-id="96928-108">Esempio 1: creare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="96928-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="96928-109">Questo comando crea un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="96928-109">This command creates a management group.</span></span>

## <span data-ttu-id="96928-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96928-110">PARAMETERS</span></span>

### <span data-ttu-id="96928-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="96928-111">-Context</span></span>
<span data-ttu-id="96928-112">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="96928-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96928-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96928-113">-DefaultProfile</span></span>
<span data-ttu-id="96928-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96928-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96928-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="96928-115">-Description</span></span>
<span data-ttu-id="96928-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="96928-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="96928-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="96928-117">-ExternalId</span></span>
<span data-ttu-id="96928-118">Per i gruppi esterni, questa proprietà contiene l'ID del gruppo dal provider di identità esterna, ad esempio Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; in caso contrario, il valore è null.</span><span class="sxs-lookup"><span data-stu-id="96928-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96928-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="96928-119">-GroupId</span></span>
<span data-ttu-id="96928-120">Specifica l'identificatore del nuovo gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="96928-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="96928-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="96928-121">-Name</span></span>
<span data-ttu-id="96928-122">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="96928-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="96928-123">-Digitare</span><span class="sxs-lookup"><span data-stu-id="96928-123">-Type</span></span>
<span data-ttu-id="96928-124">Tipo di gruppo.</span><span class="sxs-lookup"><span data-stu-id="96928-124">Group Type.</span></span> <span data-ttu-id="96928-125">Gruppo personalizzato è un gruppo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="96928-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="96928-126">Gruppo di sistemi include amministratore, sviluppatori e Guest.</span><span class="sxs-lookup"><span data-stu-id="96928-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="96928-127">Non è possibile creare o aggiornare un gruppo di sistema.</span><span class="sxs-lookup"><span data-stu-id="96928-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="96928-128">Gruppo esterno sono i gruppi provenienti da provider di identità esterni come Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="96928-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="96928-129">Questo parametro è facoltativo e per impostazione predefinita viene considerato un gruppo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="96928-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96928-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96928-130">CommonParameters</span></span>
<span data-ttu-id="96928-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96928-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96928-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96928-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96928-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96928-133">INPUTS</span></span>

### <span data-ttu-id="96928-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="96928-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="96928-135">System. String</span><span class="sxs-lookup"><span data-stu-id="96928-135">System.String</span></span>

### <span data-ttu-id="96928-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroupType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="96928-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="96928-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96928-137">OUTPUTS</span></span>

### <span data-ttu-id="96928-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="96928-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="96928-139">Note</span><span class="sxs-lookup"><span data-stu-id="96928-139">NOTES</span></span>

## <span data-ttu-id="96928-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96928-140">RELATED LINKS</span></span>

[<span data-ttu-id="96928-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="96928-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="96928-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="96928-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="96928-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="96928-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


