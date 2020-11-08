---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190249"
---
# <span data-ttu-id="3ad51-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="3ad51-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="3ad51-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ad51-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad51-103">Creare una nuova istanza di DataMigration Azure ActiveDirectory dettagli dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3ad51-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="3ad51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ad51-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ad51-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ad51-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad51-106">Creare una nuova istanza di DataMigration Azure ActiveDirectory dettagli dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3ad51-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="3ad51-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ad51-107">EXAMPLES</span></span>

### <span data-ttu-id="3ad51-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ad51-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="3ad51-109">ApplicationId: "il tuo ID di AppId/Service Principal qui" AppKey: System. Security. SecureString ID tenant: "ID tenant"</span><span class="sxs-lookup"><span data-stu-id="3ad51-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="3ad51-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ad51-110">PARAMETERS</span></span>

### <span data-ttu-id="3ad51-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="3ad51-111">-AppKey</span></span>
<span data-ttu-id="3ad51-112">Chiave di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3ad51-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad51-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3ad51-113">-ApplicationId</span></span>
<span data-ttu-id="3ad51-114">ID applicazione di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3ad51-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad51-115">-DefaultProfile</span></span>
<span data-ttu-id="3ad51-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad51-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad51-117">CommonParameters</span></span>
<span data-ttu-id="3ad51-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad51-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3ad51-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad51-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad51-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ad51-120">INPUTS</span></span>

### <span data-ttu-id="3ad51-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ad51-121">None</span></span>

## <span data-ttu-id="3ad51-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ad51-122">OUTPUTS</span></span>

### <span data-ttu-id="3ad51-123">Microsoft. Azure. Commands. DataMigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="3ad51-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="3ad51-124">Note</span><span class="sxs-lookup"><span data-stu-id="3ad51-124">NOTES</span></span>

## <span data-ttu-id="3ad51-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ad51-125">RELATED LINKS</span></span>