---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181135"
---
# <span data-ttu-id="8ff00-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="8ff00-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="8ff00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ff00-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff00-103">Ottiene le credenziali della casella dati di un processo specifico</span><span class="sxs-lookup"><span data-stu-id="8ff00-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="8ff00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ff00-104">SYNTAX</span></span>

### <span data-ttu-id="8ff00-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ff00-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ff00-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ff00-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ff00-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8ff00-107">DESCRIPTION</span></span>
<span data-ttu-id="8ff00-108">Il cmdlet **Get-AzDataBoxCredential** ottiene le credenziali della casella dei dati di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="8ff00-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="8ff00-109">Le proprietà interne dell'oggetto credenziali restituito saranno diverse per tipi di SKU diversi.</span><span class="sxs-lookup"><span data-stu-id="8ff00-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="8ff00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ff00-110">EXAMPLES</span></span>

### <span data-ttu-id="8ff00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ff00-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="8ff00-112">In questo modo vengono riemersi i JobSecrets del processo specificato</span><span class="sxs-lookup"><span data-stu-id="8ff00-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="8ff00-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ff00-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="8ff00-114">In questo modo vengono riemersi i JobSecrets del processo specificato</span><span class="sxs-lookup"><span data-stu-id="8ff00-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="8ff00-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ff00-115">PARAMETERS</span></span>

### <span data-ttu-id="8ff00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff00-116">-DefaultProfile</span></span>
<span data-ttu-id="8ff00-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff00-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8ff00-118">-Name</span></span>
<span data-ttu-id="8ff00-119">Nome processo casella di dati</span><span class="sxs-lookup"><span data-stu-id="8ff00-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff00-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff00-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ff00-121">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="8ff00-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff00-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ff00-122">-ResourceId</span></span>
<span data-ttu-id="8ff00-123">ID risorsa processo casella dati</span><span class="sxs-lookup"><span data-stu-id="8ff00-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff00-124">CommonParameters</span></span>
<span data-ttu-id="8ff00-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff00-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ff00-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff00-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="8ff00-127">INPUTS</span></span>

### <span data-ttu-id="8ff00-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8ff00-128">System.String</span></span>

## <span data-ttu-id="8ff00-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ff00-129">OUTPUTS</span></span>

### <span data-ttu-id="8ff00-130">System.Collections.generic.INav'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8ff00-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8ff00-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="8ff00-131">NOTES</span></span>

## <span data-ttu-id="8ff00-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ff00-132">RELATED LINKS</span></span>
