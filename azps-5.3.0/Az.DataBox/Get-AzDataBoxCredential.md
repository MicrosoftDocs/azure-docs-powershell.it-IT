---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487752"
---
# <span data-ttu-id="b25c9-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="b25c9-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="b25c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b25c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b25c9-103">Ottiene le credenziali di databox di un processo specifico</span><span class="sxs-lookup"><span data-stu-id="b25c9-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="b25c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b25c9-104">SYNTAX</span></span>

### <span data-ttu-id="b25c9-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b25c9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b25c9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b25c9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b25c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b25c9-107">DESCRIPTION</span></span>
<span data-ttu-id="b25c9-108">Il cmdlet **Get-AzDataBoxCredential** ottiene le credenziali della databox di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="b25c9-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="b25c9-109">Le proprietà interne dell'oggetto credenziali restituite saranno diverse per i diversi tipi di SKU.</span><span class="sxs-lookup"><span data-stu-id="b25c9-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="b25c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b25c9-110">EXAMPLES</span></span>

### <span data-ttu-id="b25c9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b25c9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b25c9-112">Questo restituisce il JobSecrets del processo specificato</span><span class="sxs-lookup"><span data-stu-id="b25c9-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="b25c9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b25c9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b25c9-114">Questo restituisce il JobSecrets del processo specificato</span><span class="sxs-lookup"><span data-stu-id="b25c9-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="b25c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b25c9-115">PARAMETERS</span></span>

### <span data-ttu-id="b25c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25c9-116">-DefaultProfile</span></span>
<span data-ttu-id="b25c9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b25c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25c9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b25c9-118">-Name</span></span>
<span data-ttu-id="b25c9-119">Nome processo databox</span><span class="sxs-lookup"><span data-stu-id="b25c9-119">Databox Job Name</span></span>

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

### <span data-ttu-id="b25c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="b25c9-121">Nome gruppo risorse processo databox</span><span class="sxs-lookup"><span data-stu-id="b25c9-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="b25c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b25c9-122">-ResourceId</span></span>
<span data-ttu-id="b25c9-123">ID risorsa processo databox</span><span class="sxs-lookup"><span data-stu-id="b25c9-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="b25c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25c9-124">CommonParameters</span></span>
<span data-ttu-id="b25c9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25c9-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b25c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25c9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b25c9-127">INPUTS</span></span>

### <span data-ttu-id="b25c9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b25c9-128">System.String</span></span>

## <span data-ttu-id="b25c9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b25c9-129">OUTPUTS</span></span>

### <span data-ttu-id="b25c9-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. Models. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b25c9-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b25c9-131">Note</span><span class="sxs-lookup"><span data-stu-id="b25c9-131">NOTES</span></span>

## <span data-ttu-id="b25c9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b25c9-132">RELATED LINKS</span></span>
