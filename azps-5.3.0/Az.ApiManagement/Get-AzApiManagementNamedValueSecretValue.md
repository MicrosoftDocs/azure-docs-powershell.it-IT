---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478947"
---
# <span data-ttu-id="b5b5f-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="b5b5f-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="b5b5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b5f-103">Ottiene un valore segreto del particolare valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="b5b5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b5f-104">SYNTAX</span></span>

### <span data-ttu-id="b5b5f-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5b5f-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b5f-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="b5b5f-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b5f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5b5f-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b5f-108">Ottiene un valore segreto del particolare valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="b5b5f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b5f-109">EXAMPLES</span></span>

### <span data-ttu-id="b5b5f-110">Esempio 1: ottenere il valore denominato per nome</span><span class="sxs-lookup"><span data-stu-id="b5b5f-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="b5b5f-111">Questo comando consente di ottenere i dettagli del valore denominato in base al nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="b5b5f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5b5f-112">PARAMETERS</span></span>

### <span data-ttu-id="b5b5f-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b5b5f-113">-Context</span></span>
<span data-ttu-id="b5b5f-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b5b5f-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b5b5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b5f-116">-DefaultProfile</span></span>
<span data-ttu-id="b5b5f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b5f-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="b5b5f-118">-NamedValueId</span></span>
<span data-ttu-id="b5b5f-119">Identificatore di un valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-119">Identifier of a the named value.</span></span>
<span data-ttu-id="b5b5f-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b5f-121">CommonParameters</span></span>
<span data-ttu-id="b5b5f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b5f-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5b5f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b5f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5b5f-124">INPUTS</span></span>

### <span data-ttu-id="b5b5f-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b5b5f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b5b5f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b5f-126">System.String</span></span>

## <span data-ttu-id="b5b5f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b5f-127">OUTPUTS</span></span>

### <span data-ttu-id="b5b5f-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="b5b5f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="b5b5f-129">Note</span><span class="sxs-lookup"><span data-stu-id="b5b5f-129">NOTES</span></span>

## <span data-ttu-id="b5b5f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b5f-130">RELATED LINKS</span></span>
