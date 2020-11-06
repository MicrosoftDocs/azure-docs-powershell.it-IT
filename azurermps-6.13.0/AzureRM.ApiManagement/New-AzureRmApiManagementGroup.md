---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: c5bbe6413a17707e7c25a616c3c67d6b7d5da5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519786"
---
# <span data-ttu-id="50b08-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50b08-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="50b08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50b08-102">SYNOPSIS</span></span>
<span data-ttu-id="50b08-103">Crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="50b08-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50b08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50b08-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b08-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b08-105">DESCRIPTION</span></span>
<span data-ttu-id="50b08-106">Il cmdlet **New-AzureRmApiManagementGroup** crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="50b08-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="50b08-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50b08-107">EXAMPLES</span></span>

### <span data-ttu-id="50b08-108">Esempio 1: creare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="50b08-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="50b08-109">Questo comando crea un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50b08-109">This command creates a management group.</span></span>

## <span data-ttu-id="50b08-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50b08-110">PARAMETERS</span></span>

### <span data-ttu-id="50b08-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="50b08-111">-Context</span></span>
<span data-ttu-id="50b08-112">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="50b08-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="50b08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b08-113">-DefaultProfile</span></span>
<span data-ttu-id="50b08-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50b08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b08-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b08-115">-Description</span></span>
<span data-ttu-id="50b08-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50b08-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="50b08-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="50b08-117">-ExternalId</span></span>
<span data-ttu-id="50b08-118">Per i gruppi esterni, questa proprietà contiene l'ID del gruppo dal provider di identità esterna, ad esempio Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; in caso contrario, il valore è null.</span><span class="sxs-lookup"><span data-stu-id="50b08-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="50b08-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="50b08-119">-GroupId</span></span>
<span data-ttu-id="50b08-120">Specifica l'identificatore del nuovo gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50b08-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="50b08-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="50b08-121">-Name</span></span>
<span data-ttu-id="50b08-122">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50b08-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="50b08-123">-Digitare</span><span class="sxs-lookup"><span data-stu-id="50b08-123">-Type</span></span>
<span data-ttu-id="50b08-124">Tipo di gruppo.</span><span class="sxs-lookup"><span data-stu-id="50b08-124">Group Type.</span></span> <span data-ttu-id="50b08-125">Gruppo personalizzato è un gruppo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="50b08-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="50b08-126">Gruppo di sistemi include amministratore, sviluppatori e Guest.</span><span class="sxs-lookup"><span data-stu-id="50b08-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="50b08-127">Non è possibile creare o aggiornare un gruppo di sistema.</span><span class="sxs-lookup"><span data-stu-id="50b08-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="50b08-128">Gruppo esterno sono i gruppi provenienti da provider di identità esterni come Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50b08-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="50b08-129">Questo parametro è facoltativo e per impostazione predefinita viene considerato un gruppo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="50b08-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="50b08-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b08-130">CommonParameters</span></span>
<span data-ttu-id="50b08-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b08-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b08-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b08-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b08-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50b08-133">INPUTS</span></span>

### <span data-ttu-id="50b08-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="50b08-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50b08-135">System. String</span><span class="sxs-lookup"><span data-stu-id="50b08-135">System.String</span></span>

### <span data-ttu-id="50b08-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroupType, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50b08-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="50b08-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50b08-137">OUTPUTS</span></span>

### <span data-ttu-id="50b08-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50b08-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="50b08-139">Note</span><span class="sxs-lookup"><span data-stu-id="50b08-139">NOTES</span></span>

## <span data-ttu-id="50b08-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50b08-140">RELATED LINKS</span></span>

[<span data-ttu-id="50b08-141">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50b08-141">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="50b08-142">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50b08-142">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="50b08-143">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50b08-143">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


