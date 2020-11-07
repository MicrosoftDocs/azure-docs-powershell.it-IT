---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685134"
---
# <span data-ttu-id="ecfda-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecfda-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="ecfda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecfda-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfda-103">Crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ecfda-103">Creates an API management group.</span></span>

## <span data-ttu-id="ecfda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecfda-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecfda-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfda-106">Il cmdlet **New-AzApiManagementGroup** crea un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ecfda-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="ecfda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecfda-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfda-108">Esempio 1: creare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="ecfda-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="ecfda-109">Questo comando crea un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ecfda-109">This command creates a management group.</span></span>

## <span data-ttu-id="ecfda-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecfda-110">PARAMETERS</span></span>

### <span data-ttu-id="ecfda-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ecfda-111">-Context</span></span>
<span data-ttu-id="ecfda-112">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ecfda-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ecfda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfda-113">-DefaultProfile</span></span>
<span data-ttu-id="ecfda-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfda-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecfda-115">-Description</span></span>
<span data-ttu-id="ecfda-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ecfda-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="ecfda-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="ecfda-117">-ExternalId</span></span>
<span data-ttu-id="ecfda-118">Per i gruppi esterni, questa proprietà contiene l'ID del gruppo dal provider di identità esterna, ad esempio Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; in caso contrario, il valore è null.</span><span class="sxs-lookup"><span data-stu-id="ecfda-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="ecfda-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ecfda-119">-GroupId</span></span>
<span data-ttu-id="ecfda-120">Specifica l'identificatore del nuovo gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ecfda-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="ecfda-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecfda-121">-Name</span></span>
<span data-ttu-id="ecfda-122">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ecfda-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="ecfda-123">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ecfda-123">-Type</span></span>
<span data-ttu-id="ecfda-124">Tipo di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ecfda-124">Group Type.</span></span> <span data-ttu-id="ecfda-125">Gruppo personalizzato è un gruppo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ecfda-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="ecfda-126">Gruppo di sistemi include amministratore, sviluppatori e Guest.</span><span class="sxs-lookup"><span data-stu-id="ecfda-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="ecfda-127">Non è possibile creare o aggiornare un gruppo di sistema.</span><span class="sxs-lookup"><span data-stu-id="ecfda-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="ecfda-128">Gruppo esterno sono i gruppi provenienti da provider di identità esterni come Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ecfda-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="ecfda-129">Questo parametro è facoltativo e per impostazione predefinita viene considerato un gruppo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ecfda-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="ecfda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfda-130">CommonParameters</span></span>
<span data-ttu-id="ecfda-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfda-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfda-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfda-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecfda-133">INPUTS</span></span>

### <span data-ttu-id="ecfda-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecfda-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecfda-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ecfda-135">System.String</span></span>

### <span data-ttu-id="ecfda-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroupType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ecfda-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ecfda-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecfda-137">OUTPUTS</span></span>

### <span data-ttu-id="ecfda-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecfda-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="ecfda-139">Note</span><span class="sxs-lookup"><span data-stu-id="ecfda-139">NOTES</span></span>

## <span data-ttu-id="ecfda-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecfda-140">RELATED LINKS</span></span>

[<span data-ttu-id="ecfda-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecfda-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="ecfda-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecfda-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="ecfda-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecfda-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


